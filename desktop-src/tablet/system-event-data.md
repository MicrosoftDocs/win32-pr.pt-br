---
description: Contém informações sobre um evento do sistema do Tablet.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Estrutura de SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708206"
---
# <a name="system_event_data-structure"></a>Estrutura de dados de \_ evento do sistema \_

Contém informações sobre um evento do sistema do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**bModifier**
</dt> <dd>

Valores de bits para os modificadores. Consulte a seção de comentários para obter mais informações.

</dd> <dt>

**wKey**
</dt> <dd>

Código de verificação do caractere de teclado.

</dd> <dt>

**xPos**
</dt> <dd>

Posição X do evento.

</dd> <dt>

**yPos**
</dt> <dd>

Posição Y do evento.

</dd> <dt>

**bCursorMode**
</dt> <dd>

O tipo de cursor que causou o evento. Consulte a seção de comentários para obter mais informações.

</dd> <dt>

**dwButtonState**
</dt> <dd>

Estado dos botões no momento do evento do sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os eventos do sistema a seguir são definidos para uso no membro **bModifier** .



| Valor               | Descrição                  |
|---------------------|------------------------------|
| ES \_ MODIFICADOr \_ Ctrl  | A tecla Control foi pressionada. |
| ES \_ MODIFICADOr \_ ALT   | A tecla Alt foi pressionada.     |
| ES \_ Shift de MODIFICADOr \_ | A tecla Shift foi pressionada.   |



 

Os eventos do sistema a seguir são definidos para uso no membro **bCursorMode** .



| Valor              | Descrição               |
|--------------------|---------------------------|
| ES \_ \_cursor normal | Indica a dica de caneta.    |
| ES \_ CURSOR do APAGAdor \_ | Indica a borracha da caneta. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IStylusPlugin:: SystemEvent**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**Método ITabletEventSink:: SystemEvent**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




