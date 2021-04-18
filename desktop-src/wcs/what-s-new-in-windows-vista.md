---
title: Novidades no Windows Vista
description: A versão 1,0 do ICM (Image Color Management) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em contextos de dispositivo do Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- WCS (sistema de cores do Windows), Windows Vista
- WCS (sistema de cores do Windows), Windows Vista
- gerenciamento de cores de imagem, Windows Vista
- gerenciamento de cores, Windows Vista
- cores, Windows Vista
- WCS (sistema de cores do Windows), sistemas operacionais
- WCS (sistema de cores do Windows), sistemas operacionais
- gerenciamento de cores de imagem, sistemas operacionais
- gerenciamento de cores, sistemas operacionais
- cores, sistemas operacionais
- ICM (Gerenciamento de cores de imagem)
- ICM (gerenciamento de cores de imagem)
- Gerenciamento de cores do Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105814619"
---
# <a name="whats-new-in-windows-vista"></a>Novidades no Windows Vista

A versão 1,0 do ICM (Image Color Management) foi fornecida no Microsoft Windows 95 e fornece recursos básicos de gerenciamento de cores em contextos de dispositivo do Windows.

O ICM versão 2,0 foi fornecido no Windows 98, no Windows Millennium Edition, no Windows 2000 e no WindowsXP e incluía uma variedade de novas funções que implementaram o gerenciamento de cores fora dos contextos de dispositivo. Essas novas funções foram adequadas para requisitos de gerenciamento de cores mais exigentes e forneciam mais controle sobre o processo de gerenciamento de cores.

Com o lançamento do Windows Vista, o ICM 2,0 agora está incluído no WCS (sistema de cores do Windows) 1,0, que adiciona mais funcionalidade. A tabela a seguir lista as novas interfaces de programação de aplicativo (API) que acompanham o Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>Novo envio de API no Windows Vista



Enumerações

Nome da API

parâmetro

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

parâmetro

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

parâmetro

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

parâmetro

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



 

 

 