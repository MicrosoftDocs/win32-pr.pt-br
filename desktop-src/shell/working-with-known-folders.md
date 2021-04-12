---
description: O sistema de pastas conhecido fornece uma maneira de interagir com determinadas pastas de perfil alto que estão presentes por padrão no Windows.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Trabalhando com pastas conhecidas em aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457196"
---
# <a name="working-with-known-folders-in-applications"></a>Trabalhando com pastas conhecidas em aplicativos

O sistema de pastas conhecido fornece uma maneira de interagir com determinadas pastas de perfil alto que estão presentes por padrão no Windows. Ele também permite as mesmas interações com pastas instaladas e registradas com o sistema de pastas conhecido por aplicativos. Este tópico discute as possíveis interações que são fornecidas pelas APIs de pasta conhecidas.

-   [Interfaces de pastas conhecidas](#known-folder-interfaces)
-   [Redirecionamento](#redirection)
-   [Tópicos relacionados](#related-topics)

> [!IMPORTANT]
> Para redirecionar os documentos, as imagens ou as pastas da área de trabalho para o OneDrive, use a movimentação de pasta conhecida do OneDrive em vez do método de redirecionamento descrito neste artigo. Para obter informações, consulte [redirecionar e mover pastas conhecidas do Windows para o onedrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Interfaces de pastas conhecidas

Há duas interfaces de pastas conhecidas: [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) e [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).

O [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) fornece muitas das funções mais gerais em relação a essas pastas. Seus métodos permitem:

-   Recupere um [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) com base no [**KNOWNFOLDERID**](knownfolderid.md)da pasta, seu nome canônico, seu caminho expresso como uma cadeia de caracteres ou seu caminho expresso como um IDList.
-   Converta uma CSIDl em seu equivalente de [**KNOWNFOLDERID**](knownfolderid.md) ou Converta um **KNOWNFOLDERID** em seu equivalente de CSIDL herdado.
-   Registre ou cancele o registro de uma pasta conhecida com o sistema.
-   Recupere todos os valores de [**KNOWNFOLDERID**](knownfolderid.md) registrados no sistema.
-   Redirecione uma pasta conhecida para um novo local.

O [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) fornece um método que permite que uma pasta seja redirecionada ao fornecer um novo caminho. Seus outros métodos obtêm informações sobre uma pasta conhecida específica, incluindo:

-   A categoria da pasta: virtual, fixa, comum ou por usuário.
-   O tipo da pasta, como compactada, documentos, imagens ou arquivos de usuário.
-   O [**KNOWNFOLDERID**](knownfolderid.md) da pasta.
-   O caminho completo da pasta como um IDList ou como uma cadeia de caracteres. Também seu caminho relativo para uma pasta pai.
-   O nome canônico da pasta.
-   A dica de ferramenta exibida para a pasta.
-   O ícone exibido para a pasta.
-   Uma descrição da pasta que explica sua finalidade e uso.
-   Se a pasta é capaz de ser redirecionada.

O [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) também fornece um método para recuperar um [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) com base na pasta. Isso permite que você associe a pasta a um manipulador, compare duas pastas e recupere os atributos da pasta, o nome de exibição e a pasta pai.

## <a name="redirection"></a>Redirecionamento

O redirecionamento de pasta é um recurso importante do sistema de pastas conhecido. Todas as pastas conhecidas da categoria [KF **comuns** da categoria \_ \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * ou KF da categoria de usuário [ **por usuário** \_ \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * são redirecionáveis. A pasta da [ **categoria virtual** KF \_ categoria \_ virtual * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * ou a [categoria **Fixed** KF \_ \_ corrigida * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)* *, no entanto, não pode ser redirecionada.

As pastas podem ser redirecionadas para outro local no mesmo computador ou em um local em uma rede. No caso de um redirecionamento de rede, a pasta pode ser armazenada em cache localmente por meio de cache do lado do cliente para fornecer acesso offline. No entanto, mesmo que exista um cache local, a própria pasta redirecionada deve ser acessada pela rede.

O redirecionamento de pasta não é novo no Windows Vista. Por exemplo, no Windows XP, algumas pastas identificadas por meio do sistema CSIDl podem ser redirecionadas por meio de uma chamada para [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) ou modificando a entrada da CSIDL no registro. No Windows Vista e posterior, o redirecionamento deve ser realizado por meio de [**IKnownFolder:: SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) ou [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).

Para determinar se uma pasta pode ser redirecionada, chame [**IKnownFolder:: GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Se a pasta não puder ser redirecionada, essa chamada poderá dar uma explicação.

Se uma pasta for redirecionada para um local de rede, os métodos [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) ainda poderão ser chamados com êxito nela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
