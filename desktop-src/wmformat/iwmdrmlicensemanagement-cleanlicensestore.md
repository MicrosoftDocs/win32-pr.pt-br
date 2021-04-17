---
title: Método IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: O método CleanLicenseStore remove licenças inutilizáveis do armazenamento de licença temporário e desfragmenta o armazenamento de licença local para melhorar o desempenho.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Formato de mídia do Windows do método CleanLicenseStore
- Método CleanLicenseStore Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CleanLicenseStore
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
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785221"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>Método IWMDRMLicenseManagement:: CleanLicenseStore

O método **CleanLicenseStore** remove licenças inutilizáveis do armazenamento de licença temporário e desfragmenta o armazenamento de licença local para melhorar o desempenho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam as opções de limpeza do repositório de licenças a serem usadas. Defina como uma das constantes na tabela a seguir.



| Constante                            | Descrição                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sincronização de \_ armazenamento de licença de limpeza do WMDRM \_ \_  | A operação de limpeza será executada de forma síncrona. Esse método não será retornado até que a operação seja concluída.                                                              |
| armazenamento de licença de limpeza do WMDRM \_ \_ \_ \_ assíncrono | A operação de limpeza será executada de forma assíncrona. Esse método retornará imediatamente. Quando a operação for concluída, o evento de mídia MELicenseStoreCleaned será enviado. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ fora\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                            | Descrição                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | O método foi bem-sucedido.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Não há nenhum repositório de licença temporário no computador cliente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente depois de ser chamado e, em seguida, gera um evento **MEWMDRMLicenseStoreCleaned** quando o processamento é concluído.

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





