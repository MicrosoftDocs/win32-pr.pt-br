---
description: Se um aplicativo isolado especificar uma dependência de assembly, o lado a lado primeiro procurará o assembly entre os assemblies compartilhados na pasta WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Sequência de pesquisa de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983466954d6cb9619d3fb0595c96f81fed7c9b73a29bfbf2f609b3f14203a957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127536"
---
# <a name="assembly-searching-sequence"></a>Sequência de pesquisa de assembly

Se um aplicativo isolado especificar uma dependência de assembly, o lado a lado primeiro procurará o assembly entre os [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) na pasta WinSxS. Se o assembly necessário não for encontrado, lado a lado, o pesquisará um assembly particular instalado em uma pasta da estrutura de diretórios do aplicativo.

Os [assemblies privados](/windows/desktop/Msi/private-assemblies) podem ser implantados nos seguintes locais na estrutura de diretórios do aplicativo:

-   Na pasta do aplicativo. Normalmente, essa é a pasta que contém o arquivo executável do aplicativo.
-   Em uma subpasta na pasta do aplicativo. A subpasta deve ter o mesmo nome que o assembly.
-   Em uma subpasta específica de idioma na pasta do aplicativo. O nome da subpasta é uma cadeia de caracteres de códigos de linguagem DHTML que indica uma linguagem ou cultura de idioma.
-   Em uma subpasta de uma subpasta específica do idioma na pasta do aplicativo. O nome da subpasta maior é uma cadeia de caracteres de códigos de linguagem DHTML que indica uma linguagem ou cultura de idioma. A subpasta mais profunda tem o mesmo nome que o assembly.

Na primeira vez em que o lado a lado procura um assembly privado, ele determina se existe uma subpasta específica do idioma na estrutura de diretório do aplicativo. Se não existir nenhuma subpasta específica do idioma, as pesquisas lado a lado do assembly privado nos seguintes locais, usando a sequência a seguir.

1.  O lado a lado pesquisa a pasta WinSxS.
2.  \\\\< > \\ appdir < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *assemblyname*>. manifest
4.  \\\\< > \\ appdir <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir <  > \\ AssemblyName < *assemblyname*>. manifest

Se uma subpasta específica a um idioma existir, a estrutura de diretório do aplicativo poderá conter o assembly privado localizado em vários idiomas. Lado a lado pesquisa as subpastas específicas do idioma para garantir que o aplicativo use o idioma especificado ou o melhor idioma disponível. As subpastas específicas do idioma são nomeadas usando uma cadeia de caracteres de códigos de idioma DHTML que especificam um idioma ou cultura de idioma. Se uma subpasta específica a um idioma existir, as pesquisas lado a lado do assembly privado nos locais a seguir usam a sequência a seguir.

1.  O lado a lado pesquisa a pasta WinSxS.
2.  \\\\< > \\ appdir < *idioma-cultura* > \\ < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *idioma-cultura* > \\ < *assemblyname*>. manifest
4.  \\\\< > \\ appdir < *idioma-cultura* > \\ <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *idioma-cultura* > \\ <  > \\ AssemblyName < *assemblyname*>. manifest

Observe que a sequência de pesquisa lado a lado localiza um arquivo DLL com o nome do assembly e para de antes de procurar um arquivo de manifesto com o nome do assembly. A maneira recomendada para lidar com um assembly privado que é uma DLL é colocar o manifesto do assembly no arquivo DLL como um recurso. A ID do recurso deve ser igual a 1 e o nome do assembly privado pode ser o mesmo que o nome da DLL. Por exemplo, se o nome da DLL for MICROSOFT.WINDOWS.MYSAMPLE.DLL, o valor do atributo name usado no elemento **AssemblyIdentity** do manifesto do assembly também poderá ser Microsoft. Windows. mysample. Como alternativa, você pode colocar o manifesto do assembly em um arquivo separado, no entanto, o nome do assembly e seu manifesto devem ser diferentes do nome da DLL. Por exemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Por exemplo, se MyApp estiver instalado na raiz da unidade c: e exigir MyAsm em francês-belga, lado a lado usa a seguinte sequência para pesquisar a melhor aproximação em uma instância localizada do MyAsm.

1.  Pesquisas lado a lado WinSxS para a versão fr-is.
2.  c: \\ MyApp \\ fr-ser \\myasm.dll
3.  c: \\ MyApp \\ fr-ser \\ MyAsm. manifest
4.  c: \\ MyApp \\ fr-ser \\ MyAsm \\myasm.dll
5.  c: \\ MyApp \\ fr-ser \\ MyAsm \\ MyAsm. manifest
6.  Pesquisas lado a lado WinSxS para a versão fr.
7.  c: \\ MyApp \\ fr \\myasm.dll
8.  c: \\ MyApp \\ fr \\ MyAsm. manifest
9.  c: \\ MyApp \\ fr \\ MyAsm \\myasm.dll
10. c: \\ MyApp \\ fr \\ MyAsm \\ MyAsm. manifest
11. Pesquisas lado a lado WinSxS para a versão en-US.
12. c: \\ MyApp \\ en-US \\myasm.dll
13. c: \\ MyApp \\ en-US \\ MyAsm. manifest
14. c: \\ MyApp \\ en-us \\ MyAsm \\myasm.dll
15. c: \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. manifest
16. Pesquisas lado a lado WinSxS para a versão en.
17. c: \\ MyApp \\ en \\myasm.dll
18. c: \\ MyApp \\ en \\ MyAsm. manifest
19. c: \\ MyApp \\ en \\ MyAsm \\myasm.dll
20. c: \\ MyApp \\ en \\ MyAsm \\ MyAsm. manifest
21. Pesquisas lado a lado WinSxS para a versão sem idioma.
22. c: \\ myapp \\myasm.dll
23. c: \\ MyApp \\ MyAsm. manifest
24. c: \\ MyApp \\ MyAsm \\myasm.dll
25. c: \\ MyApp \\ MyAsm \\ MyAsm. manifest

se a pesquisa lado a lado atingir uma versão neutra de idioma do assembly e uma versão [MUI (Interface do usuário multilíngüe)](/windows/desktop/Intl/multilingual-user-interface) do Windows estiver presente no sistema, lado a lado, tentará se associar a <*assemblyname*>. MUI. Lado a lado não tenta se associar a <*assemblyname*>. mui se a pesquisa atingir uma versão localizada do assembly. O [manifesto do assembly](assembly-manifests.md) de um assembly com neutralidade de idioma não terá um atributo de linguagem em seu elemento **AssemblyIdentity** . Se o lado a lado atingir um assembly com neutralidade de idioma e o MUI estiver instalado, o lado a lado pesquisará os seguintes locais usando a sequência a seguir para <*assemblyname*>. mui. Lado a lado usa a mesma sequência de pesquisa se o assembly for de cultura neutra, exceto <*nenhum idioma*> não for pesquisado.

1.  O lado a lado pesquisa a pasta WinSxS para <*assemblyname*>. mui.
2.  \\\\<cultura do idioma *do usuário* > \\ < *assemblyname*>. mui
3.  \\\\< > idioma \\ do < usuário *assemblyname*>. mui
4.  \\\\<cultura do idioma *do sistema* > \\ < *assemblyname*>. mui
5.  \\\\< > idioma \\ do < sistema *assemblyname*>. mui
6.  \\\\<*sem* > \\ idioma < *assemblyname*>. mui

Por exemplo, se a pesquisa lado a lado encontrar o assembly privado em c: \\ MyApp \\ MyAsm \\ MyAsm. manifest e MyAsm for um assembly com neutralidade de idioma. Lado a lado, usa a seguinte sequência para procurar MyAsm. mui. Observe que lado a lado não procurará um assembly MUI com neutralidade de idioma.

1.  Pesquisas lado a lado com WinSxS para a versão fr-is do assembly MUI.
2.  c: \\ MyApp \\ fr-ser \\myasm.mui.dll
3.  c: \\ MyApp \\ fr-ser \\ MyAsm. mui. manifest
4.  c: \\ MyApp \\ fr-ser \\ MyAsm \\myasm.mui.dll
5.  c: \\ MyApp \\ fr-ser \\ MyAsm \\ MyAsm. mui. manifest
6.  Pesquisas lado a lado são WinSxS para a versão fr do assembly MUI.
7.  c: \\ MyApp \\ fr \\myasm.mui.dll
8.  c: \\ MyApp \\ fr \\ MyAsm. mui. manifest
9.  c: \\ MyApp \\ fr \\ MyAsm \\myasm.mui.dll
10. c: \\ MyApp \\ fr \\ MyAsm \\ MyAsm. mui. manifest
11. Pesquisas lado a lado são WinSxS para a versão en-US do assembly MUI.
12. c: \\ MyApp \\ en-US \\myasm.mui.dll
13. c: \\ MyApp \\ en-US \\ MyAsm. mui. manifest
14. c: \\ MyApp \\ en-us \\ MyAsm \\myasm.mui.dll
15. c: \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. mui. manifest
16. Pesquisas lado a lado são WinSxS para a versão en do assembly MUI.
17. c: \\ MyApp \\ en \\myasm.mui.dll
18. c: \\ MyApp \\ en \\ MyAsm. mui. manifest
19. c: \\ MyApp \\ en \\ MyAsm \\myasm.mui.dll
20. c: \\ MyApp \\ en \\ MyAsm \\ MyAsm. mui. manifest

 

 
