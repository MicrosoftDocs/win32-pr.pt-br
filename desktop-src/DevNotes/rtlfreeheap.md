---
description: Libera um bloco de memória que foi alocado a partir de um heap por RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Função RtlFreeHeap (Ntifs. h)
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
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500934"
---
# <a name="rtlfreeheap-function"></a>Função RtlFreeHeap

Libera um bloco de memória que foi alocado a partir de um heap por [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

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

*HeapHandle* \[ no\]
</dt> <dd>

Um identificador para o heap cujo bloco de memória deve ser liberado. Esse parâmetro é um identificador retornado por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).

</dd> <dt>

*Sinalizadores* \[ de em, opcional\]
</dt> <dd>

Um conjunto de sinalizadores que controla aspectos de liberação de um bloco de memória. Especificar o valor a seguir substitui o valor correspondente que foi especificado no parâmetro *flags* quando o heap foi criado por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).



| Sinalizador                           | Significado                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| HEAP \_ sem \_ serialização<br/> | A exclusão mútua não será usada quando o **RtlFreeHeap** estiver acessando o heap. <br/> |



 

</dd> <dt>

*HeapBase* \[ no\]
</dt> <dd>

Um ponteiro para o bloco de memória para gratuito. Esse ponteiro é retornado por [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se o bloco foi liberado com êxito; Caso contrário, **false** .

> [!Note]  
> A partir do Windows 8, o valor de retorno é digitado como **lógico**, que tem um tamanho diferente de **booliano**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| parâmetro<br/>                   | <dl> <dt>Ntifs. h (incluir Ntifs. h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
