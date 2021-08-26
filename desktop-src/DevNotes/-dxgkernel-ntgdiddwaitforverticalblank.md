---
description: Retorna o status vertical em branco do dispositivo.
ms.assetid: d09b684b-3482-424d-8a60-d123a65f9053
title: Função NtGdiDdWaitForVerticalBlank (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdWaitForVerticalBlank
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4880dad9763372f01ba1bb91def46806fe077f0a115c98f850355853c70f1d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053326"
---
# <a name="ntgdiddwaitforverticalblank-function"></a>Função NtGdiDdWaitForVerticalBlank

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Retorna o status vertical em branco do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdWaitForVerticalBlank(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_WAITFORVERTICALBLANKDATA puWaitForVerticalBlankData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ no\]
</dt> <dd>

Identificador para objeto DirectDraw do modo de kernel criado anteriormente.

</dd> <dt>

*puWaitForVerticalBlankData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ WAITFORVERTICALBLANKDATA do DD**](/windows/win32/api/ddrawi/ns-ddrawi-ddhal_waitforverticalblankdata) que contém as informações necessárias para obter o status vertical em branco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdWaitForVerticalBlank** retorna um dos seguintes códigos de retorno de chamada.



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

 

 
