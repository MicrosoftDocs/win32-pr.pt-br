---
description: O método SetPortInfo define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para uma sessão.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: Método ITMedia::SetPortInfo (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db052c631fee1427b4d31c9149a2ef68f8819d8cacb24b632dc9b2f61d198c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140309"
---
# <a name="itmediasetportinfo-method"></a>Método ITMedia::SetPortInfo

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método SetPortInfo** define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para uma sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartPort* \[ Em\]
</dt> <dd>

Porta inicial. Isso pode ser um valor no intervalo de 0 a 65535.

</dd> <dt>

*NumPorts* \[ Em\]
</dt> <dd>

Número de portas. Isso pode ser um valor no intervalo de 0 a 65535.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro StartPort ou NumPorts* não é válido.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Essa função pode enviar dados pela transmissão em formato não criptografado; portanto, alguém que está escutando na rede pode conseguir ler os dados. O risco de segurança de enviar os dados em texto não claro deve ser considerado antes de usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Itmedia**](itmedia.md)
</dt> </dl>

 

 




