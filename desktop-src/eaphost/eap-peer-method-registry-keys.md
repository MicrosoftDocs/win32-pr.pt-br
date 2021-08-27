---
title: Valores do Registro de Método Par de EAP
description: Saiba mais sobre os valores específicos do Registro necessários para métodos pares de EAP. Consulte uma lista de valores do Registro e veja recursos adicionais disponíveis.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee42360689a74b3cd11628e6114e80532000b95f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476632"
---
# <a name="eap-peer-method-registry-values"></a>Valores do Registro de Método Par de EAP

Valores específicos do Registro são necessários para métodos pares de EAP.

## <a name="eap-peer-method-dll-paths"></a>Caminhos de DLL do método par EAP

O caminho a seguir especifica o local do Registro para DLLs de método par EAP regulares.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ *&lt; &gt; AuthorId* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método EAP dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e **um EapTypeId** de "40", aparece da seguinte forma.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ 311 \\ 40**

O caminho a seguir especifica o local do Registro para DLLs de método EAP estendidas.

> [!Note]  
> Há suporte para DLLs de método EAP estendidas Windows Vista com Service Pack 1 (SP1) ou posterior.

 

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método EAP dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **VendorId** de "311" e um **EapTypeId** de "40", aparece da seguinte forma.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6.2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores do Registro

Os seguintes valores de registro de método par EAPHost são necessários.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Os seguintes valores de registro de método par AP são recomendados.

-   [Propriedades](#properties)

Os seguintes valores de registro de método par AP são opcionais.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Valor Constante | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ EXPAND \_ SZ                                                                                                                                        |
| Descrição    | O caminho para a DLL que contém a implementação da caixa de diálogo de configuração do usuário. Por exemplo, %SystemRoot% \\ system32 \\ &lt; nome de \_ \_ DLL &gt;.dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Valor Constante | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Type           | REG \_ EXPAND \_ SZ                                                                                 |
| Descrição    | O caminho para a DLL do método EAP. Por exemplo, %SystemRoot% \\ system32 \\ &lt; nome de \_ \_ DLL &gt;.dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Valor Constante | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Type           | REG \_ SZ                                                              |
| Descrição    | Cadeia de caracteres que contém o nome amigável (exibição) para o método EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Valor Constante | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ EXPAND \_ SZ                                                                                                                                      |
| Descrição    | O caminho para a DLL que contém a implementação das funções de identidade do usuário. Por exemplo, %SystemRoot% \\ system32 \\ &lt; nome de \_ \_ DLL &gt;.dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Valor Constante | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ EXPAND \_ SZ                                                                                                                                                                                                            |
| Descrição    | O caminho para a DLL que contém a implementação da interface interativa do usuário usada para obter informações do usuário durante a execução do método EAP. Por exemplo, %SystemRoot% \\ system32 \\ &lt; nome de \_ \_ DLL &gt;.dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Valor Constante | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Descrição    | 1- para obter credenciais usando a caixa de diálogo de senha e domínio EAPHost genérica. 0 – para usar uma caixa de diálogo personalizada. Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo [**método EapPeerSetCredentials.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog




| Valor Constante | PeerInvokeUsernameDialog | 
|----------------|--------------------------|
| Type | REG_DWORD | 
| Descrição | <ul><li>1 – para obter credenciais usando a caixa de diálogo de nome de usuário EAPHost genérico.</li><li>0- para usar uma caixa de diálogo personalizada.</li></ul>Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo [<strong>método EapPeerSetCredentials.</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) | 




 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Valor Constante | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Type           | REG \_ DWORD                                                                                 |
| Descrição    | 0 se uma caixa de diálogo de interface do usuário de configuração for implementada para esse método; 1 se não for. |



 

### <a name="properties"></a>Propriedades



| Valor Constante | Propriedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrição    | Os bits no DWORD são definidos para indicar suporte para a propriedade . Para ver uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do Registro Authenticator método EAP](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configuração do Registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Usando EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 
