---
description: Cria uma representação no lado do kernel do objeto Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Função NtGdiDdCreateDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088919"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>Função NtGdiDdCreateDirectDrawObject

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Cria uma representação no lado do kernel do objeto Microsoft DirectDraw.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

Qualquer dispositivo de vídeo de DC para o qual o objeto do DirectDraw deve ser criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa função retornará um identificador para a representação de objeto do modo kernel; caso contrário, ele retornará **NULL**.

## <a name="remarks"></a>Comentários

Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos. Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.

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

[**DdCreateDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
