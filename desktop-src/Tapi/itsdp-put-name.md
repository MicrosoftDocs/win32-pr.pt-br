---
description: O \_ método Put name define o nome da sessão.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: 'ITSdp: método de ut_Name de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760339"
---
# <a name="itsdpput_name-method"></a>ITSdp::p \_ método de nome UT

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ Name** define o nome da sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o nome da sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pname* não é um ponteiro válido.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *pname* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp:: obter \_ nome**](itsdp-get-name.md)
</dt> </dl>

 

