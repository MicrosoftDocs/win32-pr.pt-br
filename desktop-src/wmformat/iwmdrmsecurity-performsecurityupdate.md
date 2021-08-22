---
title: Método IWMDRMSecurity PerformSecurityUpdate (Wmdrmsdk.h)
description: O método PerformSecurityUpdate inicia uma atualização de segurança para o subsistema DRM no computador local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Formato de mídia do windows do método PerformSecurityUpdate
- Método PerformSecurityUpdate windows Formato de mídia, interface IWMDRMSecurity
- Formato de mídia da interface IWMDRMSecurity , método PerformSecurityUpdate
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
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>Método IWMDRMSecurity::P erformSecurityUpdate

O **método PerformSecurityUpdate** inicia uma atualização de segurança para o subsistema DRM no computador local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Opção de atualização expressa como um dos sinalizadores a seguir.



| Sinalizador                                          | Descrição                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| SEGURANÇA WMDRM \_ \_ EXECUTAR \_ INDIV               | Faz com que o componente DRM seja individualizado somente se a versão do cliente estiver desa datada. |
| ATUALIZAÇÃO DE REVOGAÇÃO DE EXECUÇÃO DE SEGURANÇA DO WMDRM \_ \_ \_ \_ | Faz com que as listas de revogação no computador cliente sejam atualizadas.                               |
| SEGURANÇA WMDRM \_ \_ EXECUTAR FORCE \_ \_ INDIV        | Faz com que o componente DRM seja individualizado mesmo se a versão do cliente estiver atualizada.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para um objeto que pode ser usado para cancelar essa operação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente após ser chamado e gera eventos dependendo do sinalizador definido no *parâmetro dwFlags.*

Para individualização (sinalizador definido como WMDRM SECURITY PERFORM INDIV ou WMDRM SECURITY PERFORM FORCE INDIV), uma série de eventos \_ \_ \_ \_ \_ \_ \_ **MEWMDRMIndividualizationProgress** é gerada seguida por um evento **MEWMDRMIndividualizationCompleted** quando o processamento é concluído. O valor de cada um dos **eventos MEWMDRMIndividualizationProgress obtidos** chamando **IMFMediaEvent::GetValue** é um ponteiro **IUnknown.** Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMIndividualizationStatus.**](iwmdrmindividualizationstatus.md)

Para atualizar as listas de revogação (sinalizador definido como WMDRM SECURITY PERFORM REVOCATION REFRESH), um evento \_ \_ \_ \_ **MEWMDRMREvocationDownloadCompleted** é gerado quando o processamento é concluído.

> [!Note]  
> Quando **PerformSecurityUpdate** conclui a individualização, os únicos objetos existentes que refletirão o novo estado individualizado são aqueles que herdam de **IWMDRMSecurity.** Todos os outros objetos existentes não serão atualizados. Você deve liberar e re-criar quaisquer outros objetos para que eles reflitam o novo estado individualizado.

 

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente drm de Windows mídia, consulte Usando o modelo de evento [Media Foundation .](using-the-media-foundation-model.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Revogação e renovação de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**IWMDRMSecurity Interface**](iwmdrmsecurity.md)
</dt> <dt>

[**Executando a individualização de DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





