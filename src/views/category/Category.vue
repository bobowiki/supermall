<template>
  <div class="wrapper">
    
    <ul class="content">
      <button @click='btnClick'>按钮</button>
      <li>商场1</li>
      <li>商场2</li>
      <li>商场3</li>
      <li>商场4</li>
      <li>商场5</li>
      <li>商场6</li>
      <li>商场7</li>
      <li>商场8</li>
      <li>商场9</li>
      <li>商场10</li>
      <li>商场11</li>
      <li>商场12</li>
      <li>商场13</li>
      <li>商场14</li>
      <li>商场15</li>
      <li>商场16</li>
      <li>商场17</li>
      <li>商场18</li>
      <li>商场19</li>
      <li>商场20</li>
      <li>商场21</li>
      <li>商场22</li>
      <li>商场23</li>
      <li>商场24</li>
      <li>商场25</li>
      <li>商场26</li>
      <li>商场27</li>
      <li>商场28</li>
      <li>商场29</li>
      <li>商场30</li>
      <li>商场31</li>
      <li>商场32</li>
      <li>商场33</li>
      <li>商场34</li>
      <li>商场35</li>
      <li>商场36</li>
      <li>商场37</li>
      <li>商场38</li>
      <li>商场39</li>
      <li>商场40</li>
      <li>商场41</li>
      <li>商场42</li>
      <li>商场43</li>
      <li>商场44</li>
      <li>商场45</li>
      <li>商场46</li>
      <li>商场47</li>
      <li>商场48</li>
      <li>商场49</li>
      <li>商场50</li>
      <li>商场51</li>
      <li>商场52</li>
      <li>商场53</li>
      <li>商场54</li>
      <li>商场55</li>
      <li>商场56</li>
      <li>商场57</li>
      <li>商场58</li>
      <li>商场59</li>
      <li>商场60</li>
      <li>商场61</li>
      <li>商场62</li>
      <li>商场63</li>
      <li>商场64</li>
      <li>商场65</li>
      <li>商场66</li>
      <li>商场67</li>
      <li>商场68</li>
      <li>商场69</li>
      <li>商场70</li>
      <li>商场71</li>
      <li>商场72</li>
      <li>商场73</li>
      <li>商场74</li>
      <li>商场75</li>
      <li>商场76</li>
      <li>商场77</li>
      <li>商场78</li>
      <li>商场79</li>
      <li>商场80</li>
      <li>商场81</li>
      <li>商场82</li>
      <li>商场83</li>
      <li>商场84</li>
      <li>商场85</li>
      <li>商场86</li>
      <li>商场87</li>
      <li>商场88</li>
      <li>商场89</li>
      <li>商场90</li>
      <li>商场91</li>
      <li>商场92</li>
      <li>商场93</li>
      <li>商场94</li>
      <li>商场95</li>
      <li>商场96</li>
      <li>商场97</li>
      <li>商场98</li>
      <li>商场99</li>
      <li>商场100</li>
    </ul>
  </div>

</template>

<script>
import BScroll from 'better-scroll'

export default {
  name: "Category",
  data() {
    return {

    }
  },
  mounted() {
   this.scroll = new BScroll(document.querySelector('.wrapper'),{
     probeType: 3,
     pullUpLoad: true
   })
   this.scroll.on('scroll',(position) => {
    //  console.log(position);
   })
   this.scroll.on('pullingUp', () => {
     console.log('上拉加载更多');
   })
  },
  methods: {
    btnClick() {
      console.log('btnClick');
    }
  }

}
</script>

<style scoped>
  .wrapper{
    height: 150px;
    background-color: red;
    overflow: hidden;
  }
</style>