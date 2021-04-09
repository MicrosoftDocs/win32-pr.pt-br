---
description: Anexa uma superfície a outra superfície.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Função NtGdiDdCreateSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088920"
---
# <a name="ntgdiddcreatesurface-function"></a>Função NtGdiDdCreateSurface

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Anexa uma superfície a outra superfície.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ no\]
</dt> <dd>

Manipule a estrutura [**\_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o driver.

</dd> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador anterior para a mesma superfície. Usado se a superfície estiver sendo recriada após uma opção de modo.

</dd> <dt>

*puSurfaceDescription* \[ entrada, saída\]
</dt> <dd>

Ponteiro para a estrutura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que descreve a superfície ou o buffer que o driver deve criar.

</dd> <dt>

*puSurfaceGlobalData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para a [**estrutura \_ \_ global da superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície que são compartilhados globalmente com várias superfícies.

</dd> <dt>

*puSurfaceLocalData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma lista de [**estruturas \_ \_ locais de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descrevem os objetos de superfície criados pelo driver.

</dd> <dt>

*puSurfaceMoreData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**superfície de DD \_ \_ mais**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estrutura que contém dados de superfície local adicionais.

</dd> <dt>

*puCreateSurfaceData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ CREATESURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contém as informações necessárias para criar uma superfície.

</dd> <dt>

*puhSurface* \[ fora\]
</dt> <dd>

É usado pela API do DirectDraw e não deve ser preenchido pelo driver.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdCreateSurface** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

## <a name="remarks"></a>Comentários

É recomendável que seu aplicativo chame [IDirectDraw7:: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) em vez de usar essa função.

Ao criar uma cadeia de superfícies anexadas, como uma cadeia de permuta ou cadeia ou mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) deve ser chamado para cada superfície primeiro. Em seguida, chame [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) para anexá-los. Por fim, chame **NtGdiDdCreateSurface** para a primeira superfície somente na cadeia. Nesse caso, *hSurface* seria o identificador retornado por **NtGdiDdCreateSurfaceObject** para a primeira superfície na cadeia.

**NtGdiDdCreateSurface** só deve ser chamado para criar superfícies em memória de vídeo local e não local. Ele nunca deve ser chamado para criar superfícies de memória do sistema. Para criar superfícies de memória do sistema, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) em vez disso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
