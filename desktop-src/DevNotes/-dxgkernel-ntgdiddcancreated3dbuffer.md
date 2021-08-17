---
description: Determina se o driver pode criar um comando no nível do driver ou um buffer de vértice da descrição especificada.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: Função NtGdiDdCanCreateD3DBuffer (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 777d22347c6a922407ef423a076ab3c1f876854b6c3aaf6aee7394aa3480f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956725"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a>Função NtGdiDdCanCreateD3DBuffer

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Determina se o driver pode criar um comando no nível do driver ou um buffer de vértice da descrição especificada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ Em\]
</dt> <dd>

Lidar com a [**estrutura GLOBAL DD \_ DIRECTDRAW \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o objeto DirectDraw.

</dd> <dt>

*puCanCreateSurfaceData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura DD \_ CANCREATESURFACEDATA.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) Essa estrutura contém as informações necessárias para o driver determinar se um comando ou buffer de vértice pode ser criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdCanCreateD3DBuffer** retorna um dos códigos de retorno de chamada a seguir.



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

 

 
