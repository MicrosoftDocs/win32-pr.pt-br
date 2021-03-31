---
title: Valores de registro do método de autenticador EAP
description: Saiba mais sobre os valores de registro do método de autenticador EAP. Esses valores de registro específicos são necessários para métodos de autenticador EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917690"
---
# <a name="eap-authenticator-method-registry-values"></a>Valores de registro do método de autenticador EAP

Valores de registro específicos são necessários para métodos de autenticador EAP.

## <a name="eap-authenticator-method-dll-paths"></a>Caminhos de DLL do método de autenticador EAP

O caminho a seguir especifica o local do registro para DLLs de método de autenticador EAP regulares.

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método de autenticador EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e um **EapTypeId** de "40", aparece da seguinte maneira.

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ 311 \\ 40**

O caminho a seguir especifica o local do registro para as DLLs do método de autenticador EAP estendido.

**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorID &gt;* VendorID \\ * &lt;&gt;***

Por exemplo, um caminho de registro de instalação do método de autenticador EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **vendorid** de "311" e um **EapTypeId** de "40", aparece da seguinte maneira.

**HKLM \\ System \\ ccs \\ Services \\ Eaphost \\ métodos \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6,2 do [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores do registro

Os seguintes valores de registro de método de autenticador são obrigatórios.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Além dos valores de registro acima, o valor do registro do método autenticador a seguir é recomendado.

-   [Propriedades](#properties)

Os valores de registro do método de autenticador restantes são opcionais.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Valor Constante | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ expande \_ sz                                                                                               |
| Descrição    | O caminho para a DLL do método de autenticador EAP. Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Valor Constante | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Type           | REG \_ sz                                                                            |
| Descrição    | Cadeia de caracteres que contém o nome amigável (exibição) para o método de autenticador EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Valor Constante | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ sz                                                                                                                               |
| Descrição    | Cadeia de caracteres que contém o GUID de classe de configuração para esse método autenticador, no formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Propriedades



| Valor Constante | Propriedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ DWORD                                                                                                                                                  |
| Descrição    | Os bits no DWORD são definidos para indicar suporte para a propriedade. Para obter uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Valor Constante | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Type           | REG \_ DWORD                                                      |
| Descrição    | 0 se esse for um método de autenticador autônomo; 1 se não for. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do registro do método de par EAP](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configuração do registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




