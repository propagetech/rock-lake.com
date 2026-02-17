You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Rock Lake Advisors | About Us",
      "first_heading": "About Us"
    }
  },
  {
    "path": "clients.html",
    "context": {
      "title": "Rock Lake Advisors | Clients",
      "first_heading": "Partners and Clients"
    }
  },
  {
    "path": "contact.html",
    "context": {
      "title": "Rock Lake Advisors | Contact",
      "first_heading": "Contact"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c363a15baf9b3719c1570c22b012b369.css",
    "context": {
      "path": "css/c363a15baf9b3719c1570c22b012b369.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "data-protection-and-privacy-policy.html",
    "context": {
      "title": "Rock Lake Advisors | Home",
      "first_heading": "Data Protection and Privacy Policy"
    }
  },
  {
    "path": "email-disclaimer.html",
    "context": {
      "title": "Rock Lake Advisors | Home",
      "first_heading": "Email Disclaimer"
    }
  },
  {
    "path": "imgs/001de9019e9bb266d4b5353fb5f24d2f.webp",
    "context": {
      "refs": [
        {
          "alt": "Laura Hermann",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/03b4ebbb36fac36fcb077dc1ee34303c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0dff37bf9dbe700d0a385b05d8eab75b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1751732a1fc16a54954d6ac601157b4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17cbd722583fa2ba74c094e10fff279f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18139885ae924aee629beafe69683cad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/19aa4a8d1ac1378df659e4dd9521b64d.webp",
    "context": {
      "refs": [
        {
          "alt": "David Ryce",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f7d9964ac16ea707dba0dfaf0e59634.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/332daf25abf222727895d88d4aad2037.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b6ff0619ec08b38912a33f61d05add0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e3c10cdfa818fe031789bca8d9918f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a312e6ea7e2b28f5eddecda550eeb8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bd52daca8d0283f160e0d43bb1fd33b.webp",
    "context": {
      "refs": [
        {
          "alt": "Hiroshi Hamada",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c3915969b5716e7904c7f1795b0c16e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c8a090e9e8ef5e9d8c359ac6830817b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f6ab20dd3231687677930183e896b22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52e3fc398e381d4852c53aa4d7233cb0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/534f412e7f1894f6d71484bf2bb58742.webp",
    "context": {
      "refs": [
        {
          "alt": "Laurent Monod",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5fdf7d4bd2768806889d767e92237b96.webp",
    "context": {
      "refs": [
        {
          "alt": "David Keresztes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/623617108908c4778c3604a75a88cb78.webp",
    "context": {
      "refs": [
        {
          "alt": "John C. Cook",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6adcac477e2542d6b25ffb61bd083faf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/702ea97e0c16bea4f3554d71b43d7c12.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75d2a1e8945f8726c3088153e90cc038.webp",
    "context": {
      "refs": [
        {
          "alt": "Jason Yap",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d79be6411667519299102c27c25e40c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e4271da871e206f7f60fd190b43e98a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99db07dd1709aea395f74ca8e9e57195.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d6cbf1877aa0e8094efe7fa8916f44c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a092d62a3b71ab687cdea6d4a3c71d1e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1dda79ffc909149e0c67bf0dadc51f5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a362c12d4a09be65fec6f93dc004bf73.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a87bdcc58ccf156f862006c726fdc495.webp",
    "context": {
      "refs": [
        {
          "alt": "Robert (Bob) Cook",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad9c6974cfe768c198f0b1b9bfd1005a.webp",
    "context": {
      "refs": [
        {
          "alt": "Tom Rose",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aed7f8ea145d00b6d2aed29ec25f02e4.webp",
    "context": {
      "refs": [
        {
          "alt": "Andreas Tornblad",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af9239d2a7146c676c616a5b198444bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/afe8cd63b3fba9defe5d65b777504d75.webp",
    "context": {
      "refs": [
        {
          "alt": "Mark Banham",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1b398ca5e09e66e666c3626557ed85c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b46df39d3b43b66a3320271d42de3da4.webp",
    "context": {
      "refs": [
        {
          "alt": "Martin Schweikhart",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4a27cf306168b1d6beae3cd9cae6e9c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba76a9e0ef564eb0a503e2c17a33aef2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c2ada2a626eb38c4a868e70b7d871299.webp",
    "context": {
      "refs": [
        {
          "alt": "Javier Rivas CFA FIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c73a4eb0a461e4eaf8d8f95de59a9988.webp",
    "context": {
      "refs": [
        {
          "alt": "Mattias Eng",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8c5a14a6c43eda1507a512462a731f1.webp",
    "context": {
      "refs": [
        {
          "alt": "Felix Haas",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c951564c34be20991d84b44613fafbb1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d15d845e7155cd93ae938a49978bedd9.webp",
    "context": {
      "refs": [
        {
          "alt": "John Murray",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d20738b02b380283a17d37ae2a0c8baf.webp",
    "context": {
      "refs": [
        {
          "alt": "Filip Henzler",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d7efa09b4283a470ac0d0ef4e01563da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e076ef0a21e21a5cf8fd663bf78561ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e11206f38d390d8633f88debcaac1ae8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1c047c4a84cb2917e628b81e60bc7e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e3203a51442a3fc5554194ac4e9ff870.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e653f79b5f2f431851d1bfcfd33b8472.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8160bc9238becb0762482c1186415c1.webp",
    "context": {
      "refs": [
        {
          "alt": "Ivan Belga",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e995a6b777386da2ee6591dd92dc5037.webp",
    "context": {
      "refs": [
        {
          "alt": "Robert J.W. Van den broeck",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2eeb5aae8238c809f2ecfff9a5d38d8.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa138b893090457a271f587c4e126704.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fec1392ccb17892216cf0e1cb3858990.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Rock Lake Advisors | Home",
      "first_heading": "Rock Lake Advisors"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/7b55c20a596dc61a5a66f95e9a877067.js",
    "context": {
      "path": "js/7b55c20a596dc61a5a66f95e9a877067.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "people.html",
    "context": {
      "title": "Rock Lake Advisors | Management Team",
      "first_heading": "People"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.