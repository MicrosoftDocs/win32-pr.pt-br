---
title: Chaves do Registro do WCS
description: O WCS usa chaves do registro para sinalizar que determinados eventos de perfil de cor ocorreram. Os aplicativos devem consultar essas chaves do registro para o estado atualizado do perfil de cor do sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- WCS (sistema de cores do Windows), chaves do registro
- WCS (sistema de cores do Windows), chaves do registro
- gerenciamento de cores de imagem, chaves do registro
- gerenciamento de cores, chaves do registro
- cores, chaves do registro
- Referência do WCS, chaves do registro
- referência para WCS, chaves do registro
- WCS (sistema de cores do Windows), registro
- WCS (sistema de cores do Windows), registro
- gerenciamento de cores de imagem, registro
- gerenciamento de cores, registro
- cores, registro
- Referência do WCS, registro
- referência para WCS, registro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105766588"
---
# <a name="wcs-registry-keys"></a>Chaves do Registro do WCS

O WCS usa chaves do registro para sinalizar que determinados eventos de perfil de cor ocorreram. Os aplicativos devem consultar essas chaves do registro para o estado atualizado do perfil de cor do sistema.

## <a name="active-color-profile-changed"></a>Perfil de cor ativo alterado

Os aplicativos podem querer responder a eventos de alteração de perfil de cor para um dispositivo monitor; Isso garante que eles sempre tenham informações de cores precisas para seu destino, mesmo que o usuário ou outro aplicativo tenha alterado o perfil ativo para o dispositivo.

### <a name="desktop-applications"></a>Aplicativos da área de trabalho

Os aplicativos da área de trabalho devem escutar alterações no registro para determinar quando uma associação de perfil de cor foi alterada usando [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Um aplicativo deve ser registrado para alterações de associação de perfil por usuário e para alterações em todo o sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve ser inicializado com um HKEY fornecido por [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa). **RegOpenKeyEx** deve ser inicializado usando os seguintes locais de árvore do registro:



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Associações de perfil por usuário    | **HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}** |
| Associações de perfil em todo o sistema | **HKEY \_ \_ computador local \\ System sistema de \\ \\ controle CurrentControlSet \\ classe \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**                                        |



 

Quando o aplicativo é notificado sobre uma alteração na chave do registro, ele deve primeiro consultar se as associações por usuário ou para todo o sistema estão sendo usadas chamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). Em seguida, ele deve chamar [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) com o valor de escopo direito de gerenciamento de perfil de WCS para obter o novo perfil de cor ativo para o monitor. [**\_ \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) Observe que nem todas as alterações da chave do registro corresponderão a uma alteração real no perfil de cor atualmente ativo; o aplicativo visualiza verifica se o perfil retornado por **WcsGetDefaultColorProfile** foi realmente alterado.

### <a name="universal-windows-uwp-apps"></a>Aplicativos do Windows universal (UWP)

Os aplicativos universais do Windows não têm acesso às chaves do registro acima. Em vez disso, eles devem registrar um manipulador para o evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) . Esse evento é acionado sempre que o perfil de cor ativo do monitor no qual o aplicativo está sendo executado foi alterado. ColorProfileChanged leva em conta se as associações de perfil por usuário ou todo o sistema estão sendo usadas; essas informações são extraídas de aplicativos UWP.

Ao responder ao evento ColorProfileChanged, o aplicativo deve consultar o perfil ativo no momento usando [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 