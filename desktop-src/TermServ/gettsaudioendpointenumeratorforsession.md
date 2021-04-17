---
title: Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession
description: Retorna uma referência a um enumerador de ponto de extremidade de áudio para a ID de sessão especificada.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782881"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession

Retorna uma referência a um enumerador de ponto de extremidade de áudio para a ID de sessão especificada. Os consumidores deste enumerador de ponto de extremidade de áudio, como MMDevAPI.dll, chamam essa função para recuperar um enumerador de ponto de extremidade de áudio em uma sessão Serviços de Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SessionID* \[ no\]
</dt> <dd>

O identificador da sessão de Serviços de Área de Trabalho Remota.

</dd> <dt>

*ppEndpointEnumerator* \[ fora\]
</dt> <dd>

O endereço de um ponteiro para uma interface [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará **S \_ OK**.

## <a name="remarks"></a>Comentários

Essa função não está definida em um arquivo de cabeçalho. Você deve implementar e exportar essa função em seu enumerador de ponto de extremidade personalizado e usar a assinatura mostrada no bloco de sintaxe anteriormente neste tópico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>         |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Implementando um enumerador de ponto de extremidade de áudio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

