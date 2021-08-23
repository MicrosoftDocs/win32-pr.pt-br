---
title: Valores de registro Authenticator método EAP
description: Saiba mais sobre os valores Authenticator registro do método EAP. Esses valores específicos do Registro são necessários para métodos de autenticador de EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1db88a910a40519533ffddae40c1e1cc04d36b62f3d3ad6543ddd4a2999373e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984306"
---
# <a name="eap-authenticator-method-registry-values"></a>Valores de registro Authenticator método EAP

Valores específicos do Registro são necessários para métodos de autenticador de EAP.

## <a name="eap-authenticator-method-dll-paths"></a>Caminhos DLL Authenticator método EAP

O caminho a seguir especifica o local do Registro para DLLs de método de autenticador EAP regulares.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ *&lt; &gt; AuthorId* \\ * &lt; EapTypeId&gt;***

Por exemplo, um caminho de registro de instalação do método autenticador EAP dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e **um EapTypeId** de "40", aparece da seguinte forma.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ 311 \\ 40**

O caminho a seguir especifica o local do Registro para DLLs de método autenticador de EAP estendidas.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt; VendorIdType* \\ * &lt;&gt;***

Por exemplo, um caminho de registro de instalação do método autenticador de EAP dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **VendorId** de "311" e um **EapTypeId** de "40", aparece da seguinte forma.

**Métodos Eaphost do Sistema HKLM \\ \\ CCS \\ Services \\ \\ \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6.2 de [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valores do Registro

Os seguintes valores de registro do método authenticator são necessários.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Além dos valores do Registro acima, é recomendado o seguinte valor de registro do método authenticator.

-   [Propriedades](#properties)

Os valores restantes do registro do método authenticator são opcionais.

-   [ConfigCLSID](#configclsid)
-   [Autônomo Compatível](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Valor Constante | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ EXPAND \_ SZ                                                                                               |
| Descrição    | O caminho para a DLL do método autenticador de EAP. Por exemplo, %SystemRoot% \\ system32 \\ &lt; nome de \_ \_ DLL &gt;.dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Valor Constante | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                            |
| Descrição    | Cadeia de caracteres que contém o nome amigável (exibição) para o método autenticador EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Valor Constante | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ SZ                                                                                                                               |
| Descrição    | Cadeia de caracteres que contém o GUID da classe de configuração para esse método autenticador, no formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Propriedades



| Valor Constante | Propriedades                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                                                                                                                  |
| Descrição    | Os bits no DWORD são definidos para indicar suporte para a propriedade . Para ver uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>Autônomo Compatível



| Valor Constante | Autônomo Compatível                                             |
|----------------|-----------------------------------------------------------------|
| Tipo           | REG \_ DWORD                                                      |
| Descrição    | 0 se esse for um método autenticador autônomo; 1 se não for. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chaves do Registro de Método Par de EAP](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configuração do Registro para tipos de EAP expandidos](registry-keys-for-eap-methods.md)
</dt> <dt>

[Usando EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




