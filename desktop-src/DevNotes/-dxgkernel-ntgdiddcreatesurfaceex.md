---
description: Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de alça solicitado a ela.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Função NtGdiDdCreateSurfaceEx (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: ff5db8859cc339dc97f86e1b0421f662d69b85ba0f46449a1e721c1dc355d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956555"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>Função NtGdiDdCreateSurfaceEx

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de alça solicitado a ela.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ Em\]
</dt> <dd>

Identificador para o objeto DirectDraw criado pelo aplicativo.

</dd> <dt>

*hSurface* \[ Em\]
</dt> <dd>

Lidar com a superfície do DirectDraw a ser criada para o Direct3D. Esses alças são exclusivos em cada estrutura [**LOCAL \_ DD DIRECTDRAW \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diferente.

</dd> <dt>

*dwSurfaceHandle* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura DD \_ CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) que contém as informações necessárias para o driver criar a superfície.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdCreateSurfaceEx** retorna um dos seguintes códigos de retorno de chamada.



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

 

 
