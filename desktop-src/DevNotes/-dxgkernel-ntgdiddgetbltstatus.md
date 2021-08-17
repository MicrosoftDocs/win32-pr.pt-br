---
description: Consulta o status de blit da superfície especificada.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Função NtGdiDdGetBltStatus (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 488d0b28da747346b795ef7a1c5a3846d4661c0afb31c65a9e624584b8fe60e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956355"
---
# <a name="ntgdiddgetbltstatus-function"></a>Função NtGdiDdGetBltStatus

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Consulta o status de blit da superfície especificada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador para uma [estrutura \_ \_ local de superfície DD](https://msdn.microsoft.com/library/ms793861.aspx) que representa a superfície cujo status blit está sendo consultado.

</dd> <dt>

*puGetBltStatusData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [estrutura \_ GETBLTSTATUSDATA do DD](https://msdn.microsoft.com/library/ms794243.aspx) que contém as informações necessárias para executar a consulta de status blit.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdGetBltStatus** retorna um dos seguintes códigos de retorno de chamada.



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

 

 




