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
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172061"
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
| \_modificador de se \_ Ctrl  | A tecla Control foi pressionada. |
| \_modificador de se \_ ALT   | A tecla Alt foi pressionada.     |
| \_alternância de modificador se \_ | A tecla Shift foi pressionada.   |



 

Os eventos do sistema a seguir são definidos para uso no membro **bCursorMode** .



| Valor              | Descrição               |
|--------------------|---------------------------|
| \_cursor normal do se \_ | Indica a dica de caneta.    |
| \_cursor de borracha \_ se | Indica a borracha da caneta. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IStylusPlugin:: SystemEvent**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**Método ITabletEventSink:: SystemEvent**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




