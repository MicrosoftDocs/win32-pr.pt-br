---
title: Valores do registro do método de par EAP
description: Saiba mais sobre os valores de registro específicos que são necessários para métodos de par EAP. Consulte uma lista de valores do registro e exiba recursos adicionais disponíveis.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294512"
---
# <a name="eap-peer-method-registry-values"></a>Valores do registro do método de par EAP

Valores de registro específicos são necessários para métodos de par EAP.

## <a name="eap-peer-method-dll-paths"></a>Caminhos de DLL do método EAP peer

O caminho a seguir especifica o local do registro para DLLs do método EAP de mesmo nível regulares.

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e um **EapTypeId** de "40", aparece da seguinte maneira.

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ 311 \\ 40**

O caminho a seguir especifica o local do registro para as DLLs do método EAP estendido.

> [!Note]  
> As DLLs de método EAP estendidas têm suporte no Windows Vista com Service Pack 1 (SP1) ou posterior.

 

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **vendorid** de "311" e um **EapTypeId** de "40", aparece da seguinte maneira.

**HKLM \\ System \\ ccs \\ Services \\ Eaphost \\ métodos \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6,2 do [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores do registro

Os seguintes valores de registro do método de par do EAPHost são necessários.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Os seguintes valores de registro do método peer do AP são recomendados.

-   [Propriedades](#properties)

Os seguintes valores de registro do método peer do AP são opcionais.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Valor Constante | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expande \_ sz                                                                                                                                        |
| Descrição    | O caminho para a DLL que contém a implementação da caixa de diálogo de configuração do usuário. Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Valor Constante | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expande \_ sz                                                                                 |
| Descrição    | O caminho para a DLL do método EAP. Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Valor Constante | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Tipo           | REG \_ sz                                                              |
| Descrição    | Cadeia de caracteres que contém o nome amigável (exibição) para o método EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Valor Constante | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expande \_ sz                                                                                                                                      |
| Descrição    | O caminho para a DLL que contém a implementação das funções de identidade do usuário. Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Valor Constante | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ expande \_ sz                                                                                                                                                                                                            |
| Descrição    | O caminho para a DLL que contém a implementação da interface do usuário interativa usada para obter informações do usuário durante a execução do método EAP. Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Valor Constante | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Descrição    | 1-para obter credenciais usando a caixa de diálogo de senha e domínio do EAPHost genérico. 0-para usar uma caixa de diálogo personalizada. Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo método [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) . |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor Constante</th>
<th>PeerInvokeUsernameDialog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo</td>
<td>REG_DWORD</td>
</tr>
<tr class="even">
<td>Descrição</td>
<td><ul>
<li>1-para obter credenciais usando a caixa de diálogo nome de usuário do EAPHost genérico.</li>
<li>0-para usar uma caixa de diálogo personalizada.</li>
</ul>
Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo método [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials).</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Valor Constante | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                 |
| Descrição    | 0 se uma caixa de diálogo de interface de usuário de configuração for implementada para esse método; 1 se não for. |



 

### <a name="properties"></a>Propriedades



| Valor Constante | Propriedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrição    | Os bits no DWORD são definidos para indicar suporte para a propriedade. Para obter uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do registro do método de autenticador EAP](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configuração do registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 