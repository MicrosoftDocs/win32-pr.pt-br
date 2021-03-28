---
description: O Windows Vista apresenta novos cenários de armazenamento e um novo namespace de perfil de usuário.
title: Pastas conhecidas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968073"
---
# <a name="known-folders"></a>Pastas conhecidas

O Windows Vista apresenta novos cenários de armazenamento e um novo namespace de perfil de usuário. Para resolver esses novos fatores, o sistema mais antigo de se referir a pastas padrão por um valor de [**CSIDL**](csidl.md) foi substituído. A partir do Windows Vista, essas pastas são referenciadas por um novo conjunto de valores GUID chamado IDs de pasta conhecidas.

O sistema de pastas conhecido fornece estas vantagens:

-   ISVs (fornecedores independentes de software) podem estender o conjunto de IDs de pasta conhecidas com suas próprias. Eles podem definir pastas, fornecer IDs e registrá-las no sistema. Não foi possível estender os valores CSIDl.
-   Todas as pastas conhecidas em um sistema podem ser enumeradas. Nenhuma API forneceu essa funcionalidade para valores de CSIDl. Consulte [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) para obter mais informações.
-   Uma pasta conhecida adicionada por um ISV pode adicionar propriedades personalizadas que permitem que ele explique sua finalidade e uso pretendido.
-   Muitas pastas conhecidas podem ser redirecionadas para novos locais, incluindo locais de rede. No sistema CSIDl, somente a pasta **meus documentos** poderia ser redirecionada.
-   As pastas conhecidas podem ter manipuladores personalizados para uso durante a criação ou exclusão.

O sistema CSIDl e as APIs que usam valores de CSIDl ainda têm suporte para compatibilidade. No entanto, não é recomendável usá-los em qualquer desenvolvimento novo.


Os tópicos a seguir discutem as especificidades do sistema de pastas conhecidas.

-   [Trabalhando com pastas conhecidas em aplicativos](working-with-known-folders.md)
-   [Como estender pastas conhecidas com pastas personalizadas](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

As páginas de referência a seguir explicam as funções de pastas conhecidas do Win32, que podem ser usadas para recuperar o local de pastas conhecidas ou redirecioná-las para um novo local. Essas funções substituem as funções mais antigas do Win32. As novas funções são fornecidas para dar um comportamento equivalente às funções antigas, mas cada nova função também é duplicada por uma API de Component Object Model (COM).



| Nova função                                             | Substituto                                           | Equivalente COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder:: GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder:: SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

As páginas de referência a seguir explicam as APIs de pastas conhecidas do COM, que fornecem toda a funcionalidade das APIs do Win32 listadas acima, além de adicionar a capacidade de enumerar todas as pastas conhecidas, acessar propriedades de pasta conhecidas e estender o conjunto padrão de pastas conhecidas.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Um exemplo de C++ que demonstra as APIs de pasta conhecidas está incluído no SDK (Software Development Kit) do Windows. Depois de instalar o SDK do Windows em seu computador, o exemplo poderá ser encontrado em% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ shell \\ AppPlatform \\ KnownFolders.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
