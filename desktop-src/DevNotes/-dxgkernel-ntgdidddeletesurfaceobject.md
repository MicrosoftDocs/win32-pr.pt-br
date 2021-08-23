---
description: NtGdiDdDeleteSurfaceObject exclui um objeto de superfície de modo de kernel criado anteriormente.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Função NtGdiDdDeleteSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73418993e549bc3a72f1f4bc953b4f177a4b413d62f03e0c6e8b0c58b35998e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956525"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>Função NtGdiDdDeleteSurfaceObject

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

**NtGdiDdDeleteSurfaceObject** exclui um objeto de superfície de modo de kernel criado anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador para o objeto de superfície do modo de kernel criado anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.

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

[**DdDeleteSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
