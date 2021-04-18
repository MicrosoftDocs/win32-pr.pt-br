---
description: Enviado a todas as janelas de nível superior quando o sistema detecta mais de 12,5 por cento do tempo do sistema em um intervalo de 30 a 60 segundos está sendo gasto com a compactação da memória. Isso indica que a memória do sistema está baixa.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Mensagem de WM_COMPACTING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786213"
---
# <a name="wm_compacting-message"></a>\_Mensagem de compactação do WM

Enviado a todas as janelas de nível superior quando o sistema detecta mais de 12,5 por cento do tempo do sistema em um intervalo de 30 a 60 segundos está sendo gasto com a compactação da memória. Isso indica que a memória do sistema está baixa.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Essa mensagem é fornecida apenas para compatibilidade com aplicativos baseados no Windows de 16 bits.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A proporção do tempo de CPU (unidade de processamento central) gasto atualmente pela compactação da memória do sistema para o tempo de CPU atualmente gasto pelo sistema executando outras operações. Por exemplo, 0x8000 representa 50% do tempo de CPU gasto na compactação da memória.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Quando um aplicativo recebe essa mensagem, ele deve liberar o máximo de memória possível, levando em conta o nível atual de atividade do aplicativo e o número total de aplicativos em execução no sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Windows](windows.md)
</dt> </dl>

 

 
