---
title: Método AcquireLicense IWMDRMLicenseManagement (wmdrmsdk. h)
description: O método AcquireLicense adquire de forma assíncrona uma licença de uma URL especificada.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Método AcquireLicense Windows Media Format
- Método AcquireLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows da interface IWMDRMLicenseManagement, método AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793273"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>Método IWMDRMLicenseManagement:: AcquireLicense

O método **AcquireLicense** adquire de forma assíncrona uma licença de uma URL especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrURL* \[ no\]
</dt> <dd>

URL do servidor de licença do qual a licença será adquirida. Passe **NULL** para que o método analise a URL do cabeçalho de conteúdo.

</dd> <dt>

*bstrHeaderData* \[ no\]
</dt> <dd>

Cabeçalho de conteúdo a ser passado para o servidor de licença. Se *bstrURL* for **NULL**, o método analisará a URL desse cabeçalho. Se *dwFlags* estiver definido como WMDRM \_ adquirir \_ licença \_ herdada \_ não silenciosa, defina esse valor como a ID da chave em vez de todo o cabeçalho do conteúdo.

</dd> <dt>

*bstrActions* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém zero ou mais ações para as quais solicitar permissão na licença. A cadeia de caracteres deve ser formatada da seguinte maneira:

-   Cada ação deve ser definida dentro de um elemento ACTION. Os dados do elemento são a cadeia de caracteres de ação.
-   Todos os elementos de ação devem estar contidos em um elemento ACTIONlist.

    Por exemplo, a cadeia de caracteres para solicitar uma licença para reproduzir conteúdo é formatada da seguinte maneira:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores de opção de aquisição de licença. Defina como uma das constantes na tabela a seguir.



| Constante                                   | Descrição                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| licença de aquisição do WMDRM \_ \_ \_ silenciosa            | A licença será emitida diretamente pela Internet sem nenhuma confirmação do aplicativo cliente.              |
| licença de aquisição de WMDRM não \_ \_ \_ silenciosa         | O subsistema DRM criará uma solicitação de licença que será retornada de forma assíncrona para o lançamento no servidor de licença. |
| WMDRM \_ adquirir \_ licença \_ HERDAda não \_ silenciosa | O mesmo que o WMDRM \_ adquire a \_ licença \_ não silenciosa, exceto que um desafio de licença do DRM versão 1 será criado.           |



 

</dd> <dt>

*ppunkCancelationCookie* \[ fora\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é executado de forma assíncrona. Ele retorna imediatamente depois de ser chamado e, em seguida, gera um evento **MEWMDRMLicenseAcquisitionCompleted** quando o processamento é concluído. Para operações de aquisição de licença não silenciosa, o valor do evento obtido chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** . Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .

Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Aquisição de licença silenciosa**](silent-license-acquisition.md)
</dt> </dl>

 

 





