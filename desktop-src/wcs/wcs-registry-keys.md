---
title: Chaves do Registro do WCS
description: O WCS usa chaves do Registro para sinalizar que determinados eventos de perfil de cor ocorreram. Os aplicativos devem consultar essas chaves do Registro para o estado atualizado do perfil de cor do sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Sistema de Cores (WCS), chaves do Registro
- WCS (Windows Color System), chaves do Registro
- gerenciamento de cores da imagem, chaves do Registro
- gerenciamento de cores, chaves do Registro
- cores, chaves do Registro
- Referência do WCS, chaves do Registro
- referência para WCS, chaves do Registro
- Windows Sistema de Cores (WCS), Registro
- WCS (Windows color system),registro
- gerenciamento de cores da imagem, Registro
- gerenciamento de cores, registro
- colors,Registry
- Referência do WCS, registro
- referência para WCS, registro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c12047d83ccc2f80c26521a59a040fa45df0c21e9bb035efff6ed5d38e8827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814346"
---
# <a name="wcs-registry-keys"></a>Chaves do Registro do WCS

O WCS usa chaves do Registro para sinalizar que determinados eventos de perfil de cor ocorreram. Os aplicativos devem consultar essas chaves do Registro para o estado atualizado do perfil de cor do sistema.

## <a name="active-color-profile-changed"></a>Perfil de cor ativo alterado

Os aplicativos podem querer responder a eventos de alteração de perfil de cor para um dispositivo monitor; isso garante que eles sempre tenham informações de cor precisas para seu destino, mesmo que o usuário ou outro aplicativo tenha alterado o perfil ativo do dispositivo.

### <a name="desktop-applications"></a>Aplicativos da área de trabalho

Os aplicativos da área de trabalho devem escutar alterações no Registro para determinar quando as associações de perfil de cor foram alteradas usando [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Um aplicativo deve registrar-se para alterações de associação de perfil por usuário e para alterações em todo o sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve ser inicializado com uma HKEY fornecida por [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) **RegOpenKeyEx** deve ser inicializado usando os seguintes locais de árvore do Registro:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Associações de perfil por usuário    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion ICM \\ \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Associações de perfil em todo o sistema | **Classe de controle HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Quando o aplicativo é notificado sobre uma alteração de chave do Registro, ele deve primeiro consultar se as associações por usuário ou em todo o sistema estão sendo usadas chamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). Em seguida, ele deve chamar [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) com o valor correto de ESCOPO de GERENCIAMENTO DE [**PERFIL do WCS \_ \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) para obter o novo perfil de cor ativo para o monitor. Observe que nem todas as alterações de chave do Registro corresponderão a uma alteração real no perfil de cores ativo no momento; verifique se o perfil retornado por **WcsGetDefaultColorProfile** realmente foi alterado.

### <a name="universal-windows-uwp-apps"></a>Aplicativos UWP (universal Windows)

Aplicativos Windows universal não têm acesso às chaves do Registro acima. Em vez disso, eles devem registrar um manipulador para o [**evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation) Esse evento é ativos sempre que o perfil de cor ativo para o monitor no qual o aplicativo está sendo executado foi alterado. ColorProfileChanged leva em conta se as associações de perfil por usuário ou de todo o sistema estão sendo usadas; essas informações são abstraídos de aplicativos UWP.

Ao responder ao evento ColorProfileChanged, o aplicativo deve consultar o perfil ativo no momento usando [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 