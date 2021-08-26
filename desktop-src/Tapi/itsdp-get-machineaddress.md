---
description: O método \_ get MachineAddress obtém o endereço do computador do host de origem.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: Método ITSdp::get_MachineAddress (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e4d849c17d6c371a6edc927679e2ba6af344fbf8515310eb22b27ba4abeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012926"
---
# <a name="itsdpget_machineaddress-method"></a>Método ITSdp::get \_ MachineAddress

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get MachineAddress** obtém o endereço do computador do host de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMachineAddress* \[ out\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o endereço do computador do host de conferência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                        |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro ppMachineAddres* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                      |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o *parâmetro ppMachineAddress.*

O *parâmetro ppMachineAddress* pode ser retornado como um nome DNS ("JohnSmith.workinghard.microsoft.com") ou um endereço IP ("10.111.222.111").

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

