---
title: Método IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: O método PerformSecurityUpdate inicia uma atualização de segurança para o subsistema DRM no computador local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Formato de mídia do Windows do método PerformSecurityUpdate
- Método PerformSecurityUpdate Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8521497c1e2bca1bb2ae11349a4829c22c8b092a4cd0034008b314a7b69adb6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707896"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity: método erformSecurityUpdate de:P

O método **PerformSecurityUpdate** inicia uma atualização de segurança para o subsistema DRM no computador local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Opção de atualização expressa como um dos sinalizadores a seguir.



| Sinalizador                                          | Descrição                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| segurança do WMDRM \_ \_ executar \_ indiv               | Faz com que o componente DRM seja individualizado somente se a versão do cliente estiver desatualizada. |
| segurança do WMDRM \_ \_ executar \_ atualização de revogação \_ | Faz com que as listas de revogação no computador cliente sejam atualizadas.                               |
| segurança do WMDRM \_ \_ executar \_ forçar \_ indiv        | Faz com que o componente DRM seja individualizado mesmo que a versão do cliente esteja atualizada.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para um objeto que pode ser usado para cancelar esta operação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente depois de ser chamado e, em seguida, gera eventos dependendo do sinalizador definido no parâmetro *dwFlags* .

Para individualização (sinalizador definido como \_ segurança WMDRM \_ Execute \_ indiv ou WMDRM \_ Security \_ Execute \_ Force \_ indiv), uma série de eventos **MEWMDRMIndividualizationProgress** é gerada seguida por um evento **MEWMDRMIndividualizationCompleted** quando o processamento é concluído. O valor de cada um dos eventos **MEWMDRMIndividualizationProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** . Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .

Para atualizar as listas de revogação (sinalizador definido como WMDRM \_ Security \_ perform \_ Revocation \_ Refresh), um evento **MEWMDRMREvocationDownloadCompleted** é gerado quando o processamento é concluído.

> [!Note]  
> Quando o **PerformSecurityUpdate** conclui a individualização, os únicos objetos existentes que refletirão o novo estado individual são aqueles que herdam de **IWMDRMSecurity**. Todos os outros objetos existentes não serão atualizados. Você deve liberar e recriar outros objetos para que eles reflitam o novo estado individual.

 

para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM de mídia Windows, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Revogação e renovação de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**Executando individualização de DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





