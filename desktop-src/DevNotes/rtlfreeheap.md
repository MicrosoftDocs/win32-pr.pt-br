---
description: Libera um bloco de memória que foi alocado de um heap por RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Função RtlFreeHeap (Ntifs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538066"
---
# <a name="rtlfreeheap-function"></a>Função RtlFreeHeap

Libera um bloco de memória que foi alocado de um heap por [**RtlAllocateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)

## <a name="syntax"></a>Sintaxe


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HeapHandle* \[ Em\]
</dt> <dd>

Um alça para o heap cujo bloco de memória deve ser liberado. Esse parâmetro é um handle retornado por [**RtlCreateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)

</dd> <dt>

*Sinalizadores* \[ in, opcional\]
</dt> <dd>

Um conjunto de sinalizadores que controla aspectos da liberação de um bloco de memória. Especificar o valor a seguir substitui o valor correspondente especificado no parâmetro *Flags* quando o heap foi criado por [**RtlCreateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)



| Sinalizador                           | Significado                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| HEAP \_ SEM \_ SERIALIZAR<br/> | A exclusão mútua não será usada **quando RtlFreeHeap** estiver acessando o heap. <br/> |



 

</dd> <dt>

*HeapBase* \[ Em\]
</dt> <dd>

Um ponteiro para o bloco de memória a ser liberado. Esse ponteiro é retornado por [**RtlAllocateHeap.**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o bloco tiver sido liberado com êxito; **FALSE caso** contrário, .

> [!Note]  
> Começando com Windows 8 o valor de retorno é digitado como **LOGICAL**, que tem um tamanho diferente de **BOOLEAN.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Cabeçalho<br/>                   | <dl> <dt>Ntifs.h (inclua Ntifs.h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDtleyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
