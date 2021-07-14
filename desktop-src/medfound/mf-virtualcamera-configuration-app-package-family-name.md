---
description: Especifica o nome da família de pacotes de aplicativos para um aplicativo de configuração de câmera virtual.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691839"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>Atributo MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME

Especifica o nome da família de pacotes de aplicativos para um aplicativo de configuração de câmera virtual. Quando fornecido, o pipeline associará o aplicativo de configuração à câmera virtual e fornecerá um ponto de lançamento dentro da página Configurações Câmera.

## <a name="data-type"></a>Tipo de dados

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Comentários

Esse atributo pode ser exposto pela fonte de mídia personalizada da câmera virtual do armazenamento de atributos de origem de mídia [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).  

Se o aplicativo de configuração ainda não estiver instalado no computador, o aplicativo Store será lançado e navegará até a página do aplicativo especificada pelo nome da família de pacotes. Caso contrário, o aplicativo instalado será lançado para o usuário.


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Build 22000<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Build 22000<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




