---
title: Método IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- WaitForCompletion do método virtual PC
- Método WaitForCompletion Virtual PC, interface IVMTask
- IVMTask interface virtual PC, método WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763456"
---
# <a name="ivmtaskwaitforcompletion-method"></a>Método IVMTask:: WaitForCompletion

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tempo limite* \[ no\]
</dt> <dd>

O tempo, em milissegundos, que esse método aguardará para a conclusão da tarefa antes de retornar o controle ao chamador. Um valor de-1 especifica que o método aguardará até que a tarefa seja concluída sem atingir o tempo limite. Outros valores de tempo limite válidos variam de 0 a 4 milhões milissegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | O parâmetro *Timeout* não é válido.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>     |



 

## <a name="remarks"></a>Comentários

O método **WaitForCompletion** coloca o thread de execução atual em suspensão até que ele retorne. A especificação de uma espera infinita (timeout =-1) não é recomendada, a menos que seja absolutamente crítica que a tarefa seja concluída em qualquer circunstância.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

