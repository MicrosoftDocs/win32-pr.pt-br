---
title: Informações sobre versão
description: Esta seção aborda o recurso de informações de versão.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- recursos, informações de versão
- informações de versão
- números de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69601c593c51a5a15a0af0706a019f135d855875f6e1ecabdb414a8a100045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733091"
---
# <a name="version-information"></a>Informações sobre versão

As informações de versão facilitam que os aplicativos instalem arquivos corretamente e permite que os programas de instalação analisem os arquivos atualmente instalados. O recurso de informações de versão contém o número de versão do arquivo, seu sistema operacional pretendido e o nome do arquivo original.

### <a name="in-this-section"></a>Nesta seção



| Name                                                               | Descrição                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Sobre informações de versão](about-version-information.md)         | Discute as funções de informações de versão.<br/>            |
| [Usando informações de versão](using-version-information.md)         | Discute como usar as funções de informações de versão.<br/> |
| [Referência de informações de versão](version-information-reference.md) | Contém a referência de API.<br/>                             |



 

### <a name="version-information-functions"></a>Funções de informações de versão



| Name                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Recupera informações de versão para o arquivo especificado. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Recupera informações de versão para o arquivo especificado.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Determina se o sistema operacional pode recuperar informações de versão para um arquivo especificado. Se as informações de versão estiverem disponíveis, [**falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) retornará o tamanho, em bytes, dessas informações. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Determina se o sistema operacional pode recuperar informações de versão para um arquivo especificado. Se as informações de versão estiverem disponíveis, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) retornará o tamanho, em bytes, dessas informações.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Determina onde instalar um arquivo com base em se ele localiza outra versão do arquivo no sistema. Os valores que [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) retorna nos buffers especificados são usados em uma chamada subsequente para a função [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) . <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Instala o arquivo especificado com base nas informações retornadas da função [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) . O [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) descompacta o arquivo, se necessário, atribui um nome de arquivo exclusivo e verifica se há erros, como arquivos desatualizados. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Recupera uma cadeia de caracteres de descrição para o idioma associado a um identificador de idioma binário especificado da Microsoft.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Recupera informações de versão especificadas do recurso de informações de versão especificado. Para recuperar o recurso apropriado, antes de chamar [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea), você deve primeiro chamar a função [**falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) e, em seguida, a função [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) . <br/> |



 

### <a name="version-information-structures"></a>Estruturas de informações de versão



| Name                                          | Descrição                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Strings**](string-str.md)                  | Descreve a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas registradas.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Descreve a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão que podem ser exibidas para uma determinada linguagem e página de código.<br/>                                                           |
| [**StringTable**](stringtable.md)            | Descreve a organização de dados em um recurso de versão de arquivo. Ele contém informações de formatação de página de código e idioma para as cadeias de caracteres especificadas pelo membro **filho** . Uma página de código é um conjunto de caracteres ordenados.<br/> |
| [**Var**](var-str.md)                        | Descreve a organização de dados em um recurso de versão de arquivo. Normalmente, ele contém uma lista de pares de identificadores de página de código e de idioma para os quais a versão do aplicativo ou DLL dá suporte.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Descreve a organização de dados em um recurso de versão de arquivo. Ele contém informações de versão não dependentes de uma combinação de linguagem de código e de idioma específico.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contém informações de versão sobre um arquivo. Essas informações são independentes da página de código e do idioma. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Descreve a organização de dados em um recurso de versão de arquivo. É a estrutura raiz que contém todas as outras estruturas de informações de versão de arquivo.<br/>                                                                    |



 

 

 





