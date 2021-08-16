---
title: Método IWMDRMLicenseManagement CleanLicenseStore (Wmdrmsdk.h)
description: O método CleanLicenseStore remove licenças inutilizáveis do repositório de licenças temporárias e desfragmenta o repositório de licenças local para melhorar o desempenho.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Formato de mídia do windows do método CleanLicenseStore
- Formato de mídia do windows do método CleanLicenseStore, interface IWMDRMLicenseManagement
- IWMDRMLicenseManagement interface windows Formato de mídia, método CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846944"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>Método IWMDRMLicenseManagement::CleanLicenseStore

O **método CleanLicenseStore** remove licenças inutilizáveis do repositório de licenças temporárias e desfragmenta o repositório de licenças local para melhorar o desempenho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Sinalizadores que especificam as opções de limpeza do armazenamento de licenças a usar. De definido como uma das constantes na tabela a seguir.



| Constante                            | Descrição                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SINCRONIZAÇÃO DO \_ ARMAZENAMENTO DE \_ LICENÇAS \_ LIMPAS DO \_ WMDRM  | A operação limpa será executada de forma síncrona. Esse método não retornará até que a operação seja concluída.                                                              |
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ ASYNC | A operação limpa será executada de forma assíncrona. Esse método retornará imediatamente. Quando a operação for concluída, o evento de mídia MELicenseStoreCleaned será enviado. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                            | Descrição                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | O método foi bem-sucedido.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Não há nenhum armazenamento de licença temporário no computador cliente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente após ser chamado e gera um **evento MEWMDRMLicenseStoreCleaned** quando o processamento é concluído.

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente drm de Windows mídia, consulte Usando o modelo de evento [Media Foundation .](using-the-media-foundation-model.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicenseManagement Interface**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





