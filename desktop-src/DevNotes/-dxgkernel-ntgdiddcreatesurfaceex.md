---
description: Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de identificador solicitado a ela.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Função NtGdiDdCreateSurfaceEx (Ntgdi. h)
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
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088918"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>Função NtGdiDdCreateSurfaceEx

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de identificador solicitado a ela.

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

*hDirectDraw* \[ no\]
</dt> <dd>

Identificador para o objeto do DirectDraw criado pelo aplicativo.

</dd> <dt>

*hSurface* \[ no\]
</dt> <dd>

Manipule a superfície do DirectDraw a ser criada para o Direct3D. Esses identificadores são exclusivos em cada [**estrutura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diferente do DIRECTDRAW do DD.

</dd> <dt>

*dwSurfaceHandle* \[ no\]
</dt> <dd>

Identificador para uma [**estrutura \_ CREATESURFACEEXDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) que contém as informações necessárias para o driver criar a superfície.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdCreateSurfaceEx** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

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

 

 
