---
title: Valores do registro do protocolo de autenticação
description: O software de instalação para a DLL EAP pode criar os seguintes valores de registro abaixo de eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0822e7abb62aad136a3abbe36ee92f5b6f1ec9fbeabd6426c039f05c1f752d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739556"
---
# <a name="authentication-protocol-registry-values"></a>Valores do registro do protocolo de autenticação

O software de instalação para a DLL EAP pode criar os seguintes valores de registro abaixo de **&lt; eaptypeid &gt;**. Esses valores de registro são definidos no arquivo de cabeçalho Raseapif. h. Os valores de **RAS_EAP_VALUENAME_PATH** e **RAS_EAP_VALUENAME_FRIENDLY_NAME** são obrigatórios. O software de instalação também pode criar outras chaves e valores. Eles podem ser usados pelo próprio protocolo de autenticação. Para obter mais informações e um exemplo de configuração de registro, consulte [exemplo de valores de registro](registry-values-example.md).

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Encontrei

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Valor constante | Caminho                               |
|----------------|------------------------------------|
| Type           | REG_EXPAND_SZ                    |
| Descrição    | Especifica o caminho para a DLL de EAP. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Valor constante | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_SZ                                                                                                                                                           |
| Descrição    | Especifica um nome amigável para o protocolo de autenticação. Esse nome aparece na interface do usuário do aplicativo EAP para implementações discadas e sem fio. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Valor constante | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                   |
| Descrição    | Especifica o caminho para a DLL que implementa a interface do usuário de configuração no cliente, porque essa interface do usuário é apenas para o cliente. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Valor constante | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| Tipo           | REG_BINARY                                                           |
| Descrição    | Especifica os dados de configuração padrão para o protocolo de autenticação. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Valor constante | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                               |
| Descrição    | Especifica se o usuário deve fornecer dados de configuração na interface do usuário do aplicativo de cliente EAP. Se esse valor for 1, o usuário não poderá sair da interface do usuário do aplicativo do cliente EAP sem fornecer dados de configuração. O valor padrão é 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Valor constante | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| Tipo           | REG_SZ                                                       |
| Descrição    | Especifica a ID de classe da interface do usuário de configuração no servidor. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Valor constante | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                        |
| Descrição    | Especifica o caminho para a DLL que implementa as funções para obter a identidade do usuário no cliente, porque essa interface do usuário é apenas para o cliente. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Valor constante | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_EXPAND_SZ                                                                                                                 |
| Descrição    | Especifica o caminho para a DLL que implementa a interface do usuário interativa no cliente, pois essa interface do usuário é apenas para o cliente. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Valor constante | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                             |
| Descrição    | especifica se o RAS deve exibir a caixa de diálogo de nome de usuário Windows NT/Windows 2000 padrão (valor de 1) ou invocar [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valor de 0). O valor padrão é 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Valor constante | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                  |
| Descrição    | especifica se o RAS deve exibir a caixa de diálogo de senha Windows NT/Windows 2000 padrão. Se esse valor existir e for 0, o RAS não exibirá a caixa de diálogo de senha. O valor padrão é 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Valor constante | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                    |
| Descrição    | Se esse valor for 1, o protocolo de autenticação poderá gerar chaves para o estilo de criptografia MPPE (criptografia ponto a ponto) da Microsoft. Os valores possíveis são 0 ou 1. O valor padrão é 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Valor constante | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                     |
| Descrição    | especifica se esse protocolo de autenticação tem suporte em um servidor Windows 2000 autônomo. Um valor de 0 indica que não há suporte para o EAP. O valor padrão é 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Valor Constante | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                 |
| Descrição    | Especifica as várias funções às quais o EAP dá suporte. Isso indica se ele pode ser usado em um servidor ou em um cliente, se há suporte para conexões RAS (VPN) ou PEAP. O comportamento padrão é mostrar o método EAP no PEAP e no EAP. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Valor Constante | PerPolicyConfig |
|----------------|-----------------|
| Tipo           | REG_DWORD      |
| Descrição    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Esse valor de registro não está em uso.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Esse valor de registro não está em uso.

