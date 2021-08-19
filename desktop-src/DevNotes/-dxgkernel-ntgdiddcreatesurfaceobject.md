---
description: Cria um objeto de superfície do modo kernel que representa o objeto de superfície do modo de usuário referenciado por puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Função NtGdiDdCreateSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956535"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>Função NtGdiDdCreateSurfaceObject

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Cria um objeto de superfície do modo kernel que representa o objeto de superfície do modo de usuário referenciado por *puSurfaceLocal*.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* \[ no\]
</dt> <dd>

Identificador para o objeto DirectDraw do modo kernel.

</dd> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador anterior para a mesma superfície. Usado se a superfície estiver sendo recriada após uma opção de modo.

</dd> <dt>

*puSurfaceLocal* \[ no\]
</dt> <dd>

Ponteiro para a [**estrutura \_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa o objeto de superfície do modo de usuário do DirectDraw ao qual associar a memória alocada. Consulte a documentação do DDK para obter detalhes.

</dd> <dt>

*puSurfaceMore* \[ no\]
</dt> <dd>

Aponta para a [**superfície de DD \_ \_ mais**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estrutura que contém dados locais adicionais para cada objeto de superfície individual. Consulte a documentação do DDK para obter detalhes.

</dd> <dt>

*puSurfaceGlobal* \[ no\]
</dt> <dd>

Ponteiro para a [**estrutura \_ \_ global da superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície compartilhados globalmente com várias superfícies. Consulte a documentação do DDK para obter detalhes.

</dd> <dt>

*bComplete* \[ no\]
</dt> <dd>

Sinalizador de conclusão de objeto em modo kernel. Pode ser um dos valores a seguir.

<dt>



 TRUE


</dt> <dd>

Conclua todo o processamento em relação à representação do modo kernel.

</dd> <dt>



 FOR


</dt> <dd>

Crie o objeto, mas não configure dados internos, como o ponteiro de memória. Os objetos criados usando **false** podem ser anexados usando [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) e são concluídos por uma chamada para [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função retornará um identificador para a representação de superfície do modo kernel; caso contrário, ele retornará **NULL**.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
