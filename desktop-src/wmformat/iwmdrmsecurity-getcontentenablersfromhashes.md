---
title: Método IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: O método GetContentEnablersFromHashes recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Formato de mídia do Windows do método GetContentEnablersFromHashes
- Método GetContentEnablersFromHashes Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747453"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>Método IWMDRMSecurity:: GetContentEnablersFromHashes

O método **GetContentEnablersFromHashes** recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rgpbCertHashes* \[ no\]
</dt> <dd>

Matriz de hashes de certificado para obter habilitadores de conteúdo para o.

</dd> <dt>

*cCerts* \[ no\]
</dt> <dd>

Número de certificados para os quais recuperar os habilitadores de conteúdo. Este é o número de elementos na matriz *rgpbCertHashes* .

</dd> <dt>

*hResultHint* \[ no\]
</dt> <dd>

Valor de retorno recebido da operação que falhou devido a um certificado revogado. Se você não estiver chamando em resposta a uma chamada de método com falha, defina para S \_ OK.

</dd> <dt>

*prgContentEnablers* \[ fora\]
</dt> <dd>

Matriz que recebe os endereços das interfaces **IMFContentEnabler** recém-criadas. Defina como **NULL** para obter o número de habilitadores de conteúdo no parâmetro *pcContentEnablers* .

</dd> <dt>

*pcContentEnablers* \[ entrada, saída\]
</dt> <dd>

Número de elementos na matriz *prgContentEnablers* . Se *prgContentEnablers* for **NULL**, esse valor será definido como o número de habilitadores de conteúdo necessários na saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se você usar a interface **IMFContentEnabler** para renovar os componentes revogados, você deverá esclarecer o processo para o usuário. Esse esclarecimento deve ser feito porque o processo de atualização envia informações do computador cliente para um site da Microsoft.

Quando você chama **IMFContentEnabler:: AutomaticEnable**, o ativador de conteúdo inicia o navegador padrão com o endereço do serviço de atualização no site da Microsoft. Um identificador exclusivo que identifica o componente revogado é enviado para o serviço de atualização. Em seguida, o serviço redireciona o navegador para uma página da Web da qual o usuário poderá baixar e instalar a nova versão do componente revogado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





