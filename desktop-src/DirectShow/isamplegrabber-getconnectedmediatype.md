---
description: O método GetConnectedMediaType recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Método ISampleGrabber:: GetConnectedMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818055"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>Método ISampleGrabber:: GetConnectedMediaType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetConnectedMediaType` método recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pType* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) alocada pelo chamador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                                           | Descrição                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                     |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O filtro não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método copia o tipo de mídia para a estrutura do **\_ \_ tipo de mídia am** especificada por *pType*. O chamador deve liberar o bloco de formato do tipo de mídia. Você pode usar a função **CoTaskMemFree** ou a função [**FreeMediaType**](freemediatype.md) na biblioteca de classe base.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o exemplo de apoio](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




