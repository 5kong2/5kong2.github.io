## 코드 : 크롬창 -> 교육창 -> F12 -> Console에 아래 코드 복붙 & 엔터

var currentPage = nowPageNum;

function goNextPage() {
    if (currentPage <= totalPageNum) {
        PageMove2019AfterVersion(currentPage); 
        console.log(`${currentPage} 페이지를 수강완료했습니다.`);
        currentPage += 1;
        setTimeout(function() {
            goNextPage();
        }, 1000);
    } else {
        alert('강의 수강이 완료되었습니다!');
    }
}

function runKmuMacro() {
    console.log(`현재 ${currentPage} 페이지를 수강중입니다.`);

    setTimeout(function () {
        goNextPage();
    }, 1000)
}

runKmuMacro();





.
.
.
.
.
.
.
.







## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/5kong2/5kong2.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/5kong2/5kong2.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
