---
title: Novidades no Windows Vista
description: a versão 1,0 do gerenciamento de cores de imagem (ICM) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em Windows contextos de dispositivo.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows sistema de cores (WCS), Windows Vista
- WCS (Windows sistema de cores), Windows Vista
- gerenciamento de cores de imagem, Windows Vista
- gerenciamento de cores, Windows Vista
- cores, Windows Vista
- Windows Sistema de cores (WCS), sistemas operacionais
- WCS (Windows sistema de cores), sistemas operacionais
- gerenciamento de cores de imagem, sistemas operacionais
- gerenciamento de cores, sistemas operacionais
- cores, sistemas operacionais
- ICM (Gerenciamento de cores de imagem)
- ICM (gerenciamento de cores de imagem)
- Windows Gerenciamento de cores do vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f6c3313a1b7ca78f0f4d3436d7bb2017b0fa794291b4bd765651aa0321166d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670732"
---
# <a name="whats-new-in-windows-vista"></a>Novidades no Windows Vista

a versão 1,0 do gerenciamento de cores de imagem (ICM) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em Windows contextos de dispositivo.

ICM versão 2,0 foi entregue em Windows 98, Windows Millennium Edition, Windows 2000 e WindowsXP e incluía uma variedade de novas funções que implementaram o gerenciamento de cores fora dos contextos de dispositivo. Essas novas funções foram adequadas para requisitos de gerenciamento de cores mais exigentes e forneciam mais controle sobre o processo de gerenciamento de cores.

com o lançamento do Windows Vista, o ICM 2,0 agora está incluído no WCS (Windows Color System) 1,0, que adiciona mais funcionalidade. a tabela a seguir lista as novas interfaces de programação de aplicativo (API) que acompanham o Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>novo envio de API no Windows Vista



Enumerações

Nome da API

Cabeçalho

Biblioteca

[**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype)

ICM. h

mscms. lib

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

ICM. h

mscms. lib

[**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)

ICM. h

mscms. lib

[**\_escopo de \_ Gerenciamento de perfil do WCS \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

ICM. h

mscms. lib



 



Funções

Nome da API

Cabeçalho

Biblioteca

[**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

ICM. h

mscms. lib

[**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

ICM. h

mscms. lib

[**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

ICM. h

mscms. lib

[**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

ICM. h

mscms. lib

[**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

ICM. h

mscms. lib

[**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

ICM. h

mscms. lib

[**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

ICM. h

mscms. lib

[**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

ICM. h

mscms. lib

[**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

ICM. h

mscms. lib

[**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

ICM. h

mscms. lib



 



Interfaces e suas funções

Nome da API

Cabeçalho

Biblioteca

[**IDeviceModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::ColorimetricToDeviceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::D eviceToColorimetricColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetGamutBoundaryMesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetGamutBoundaryMeshSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNeutralAxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNeutralAxisSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNumChannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetPrimarySamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::SetTransformDeviceModelInfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

WcsPlugIn. h

N/D



 



Estruturas

Nome da API

Cabeçalho

Biblioteca

[**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

WcsPlugIn. h

N/D

[**GamutBoundaryDescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

WcsPlugIn. h

N/D

[**XYZColorF**](https://www.bing.com/search?q=**XYZColorF**)

WcsPlugIn. h

N/D

[**JChColorF**](https://www.bing.com/search?q=**JChColorF**)

WcsPlugIn. h

N/D

[**JabColorF**](https://www.bing.com/search?q=**JabColorF**)

WcsPlugIn. h

N/D

[**GamutShell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

WcsPlugIn. h

N/D

[**GamutShellTriangle**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

WcsPlugIn. h

N/D

[**PrimaryJabColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

WcsPlugIn. h

N/D

[**PrimaryXYZColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

WcsPlugIn. h

N/D



 

 

 