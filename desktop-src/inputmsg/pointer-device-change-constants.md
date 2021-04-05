---
title: Alteração do dispositivo do ponteiro
description: Valores que podem ser passados no parâmetro wParam da mensagem de WM_POINTERDEVICECHANGE.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918819"
---
# <a name="pointer-device-change"></a>Alteração do dispositivo do ponteiro

Valores que podem ser passados no parâmetro *wParam* da mensagem de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .

<dl> <dt>

<span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**
</dt> <dd> <dl> <dt>

0x001
</dt> <dt>



Um novo dispositivo está anexado.


</dt> </dl> </dd> <dt>

<span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**
</dt> <dd> <dl> <dt>

0x002
</dt> <dt>



Um dispositivo foi desanexado.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**
</dt> <dd> <dl> <dt>

0x004
</dt> <dt>



Orientação do dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**
</dt> <dd> <dl> <dt>

0x008
</dt> <dt>



Orientação do dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**
</dt> <dd> <dl> <dt>

0x010
</dt> <dt>



Orientação do dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**
</dt> <dd> <dl> <dt>

0x020
</dt> <dt>



Orientação do dispositivo.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**
</dt> <dd> <dl> <dt>

0x040
</dt> <dt>



O modo de exibição padrão.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**
</dt> <dd> <dl> <dt>

0x080
</dt> <dt>



Modo de exibição centralizado.


</dt> </dl> </dd> <dt>

<span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**
</dt> <dd> <dl> <dt>

0x100
</dt> <dt>



A alteração em Exibir para o mapeamento de digitalizador.


</dt> </dl> </dd> <dt>

<span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**
</dt> <dd> <dl> <dt>

0x200
</dt> <dt>



Resolução de vídeo.


</dt> </dl> </dd> <dt>

<span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



A origem de exibição.


</dt> </dl> </dd> <dt>

<span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**
</dt> <dd> <dl> <dt>

0x800
</dt> <dt>



A taxa de proporção de exibição.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





