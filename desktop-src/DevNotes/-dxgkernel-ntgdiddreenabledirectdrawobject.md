---
description: Habilita novamente um objeto de dispositivo do modo kernel do Microsoft DirectDraw após uma opção de modo.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Função NtGdiDdReenableDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089438"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>Função NtGdiDdReenableDirectDrawObject

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Habilita novamente um objeto de dispositivo do modo kernel do Microsoft DirectDraw após uma opção de modo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* \[ no\]
</dt> <dd>

O objeto DirectDraw que precisa ser habilitado novamente.

</dd> <dt>

*pubNewMode* \[ entrada, saída\]
</dt> <dd>

Ponteiro para um BOOL que será preenchido com um valor que representa se o modo de exibição foi alterado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido (o dispositivo pode ser habilitado novamente), essa função retornará **true**. Caso contrário (por exemplo, o driver de vídeo foi alterado), ele retornará **false**.

## <a name="remarks"></a>Comentários

Depois que o objeto tiver sido reabilitado, os recursos do dispositivo poderão ser consultados novamente por meio de uma chamada para [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

Os aplicativos são aconselhados a usar as APIs do DirectDraw ou do [Direct3D](../direct3d10/d3d10-graphics-reference.md) versão 8, que automatizam e abstraem esse processo de maneira independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
