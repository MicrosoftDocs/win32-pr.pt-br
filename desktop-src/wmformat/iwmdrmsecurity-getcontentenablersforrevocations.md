---
title: Método IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: O método GetContentEnablersForRevocations recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Formato de mídia do Windows do método GetContentEnablersForRevocations
- Método GetContentEnablersForRevocations Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747454"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>Método IWMDRMSecurity:: GetContentEnablersForRevocations

O método **GetContentEnablersForRevocations** recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rgpbCerts* \[ no\]
</dt> <dd>

Matriz de certificados para recuperar habilitadores de conteúdo para o. O número de elementos na matriz deve ser especificado por *cCerts*.

</dd> <dt>

*rgpdwCertSizes* \[ no\]
</dt> <dd>

Matriz que contém os tamanhos dos certificados na matriz *rgpbCerts* . O número de elementos na matriz deve ser especificado por *cCerts*.

</dd> <dt>

*rgpguidCerts* \[ no\]
</dt> <dd>

Matriz que contém os tipos de certificados na matriz *rgpbCerts* . O número de elementos na matriz deve ser especificado por *cCerts*. Para cada elemento da matriz, use um dos valores a seguir.



| Constante de GUID                 | Descrição                                                    |
|-------------------------------|----------------------------------------------------------------|
| \_aplicativo WMDRM RErevocationtype \_    | Especifica um certificado de aplicativo.                          |
| \_dispositivo WMDRM RErevocationtype \_ | Especifica um certificado de dispositivo.                                |
| WMDRM \_ RErevocationtype \_ CARDEA | Especifica um certificado de Windows Media DRM para dispositivos de rede. |



 

</dd> <dt>

*cCerts* \[ no\]
</dt> <dd>

Número de certificados para os quais recuperar os habilitadores de conteúdo. Esse é o número de elementos na matriz *rgpbCerts* , a matriz *rgpdwCertSizes* e a matriz *rgpguidCerts* .

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

[**Revogação e renovação de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





