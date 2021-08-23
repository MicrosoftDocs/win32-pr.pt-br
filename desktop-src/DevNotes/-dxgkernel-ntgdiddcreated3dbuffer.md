---
description: Usado para criar um comando no nível do driver ou buffer de vértice da descrição especificada.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Função NtGdiDdCreateD3DBuffer (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 55e28e50f10ced5380685cbdb5016363a77adc7e61d2df201565d18f4794fcf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956695"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>Função NtGdiDdCreateD3DBuffer

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Usado para criar um comando no nível do driver ou buffer de vértice da descrição especificada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ Em\]
</dt> <dd>

Lidar com a [**estrutura GLOBAL DD \_ DIRECTDRAW \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o driver.

</dd> <dt>

*hSurface* \[ in, out\]
</dt> <dd>

Ponteiro para uma matriz de alças de superfície. O chamador poderá definir esses alças para os valores de alça anteriores se as superfícies estão sendo re-criadas após uma opção de modo. Esse processo é chamado de "restauração" na documentação do DirectDraw.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que descreve a superfície ou buffer que o driver deve criar.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura GLOBAL do DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície que são compartilhados globalmente com várias superfícies.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Ponteiro para uma lista de estruturas [**LOCAIS do DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descrevem os objetos de superfície criados pelo driver. Normalmente, há apenas uma entrada nessa matriz.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) que contém dados adicionais da superfície local.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contém as informações necessárias para criar o buffer.

</dd> <dt>

*puhSurface* \[ in, out\]
</dt> <dd>

É usado pela API do DirectDraw e não deve ser preenchido pelo driver.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdCreateD3DBuffer** retorna um dos códigos de retorno de chamada a seguir.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ MANIPULADO**</dt> </dl>    | O driver realizou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, DirectDraw ou Direct3D prosseguirá com a função . Caso contrário, DirectDraw ou Direct3D retornará o código de erro fornecido pelo driver e anulará a função.<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ DRIVER \_ NOTHANDLED**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se o driver precisar ter implementado um retorno de chamada específico, DirectDraw ou Direct3D relata uma condição de erro. Caso contrário, DirectDraw ou Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido executando a implementação independente de dispositivo DirectDraw ou Direct3D.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
