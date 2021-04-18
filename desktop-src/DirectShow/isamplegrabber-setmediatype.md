---
description: O método SetMediaType especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Método ISampleGrabber:: SetMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757672"
---
# <a name="isamplegrabbersetmediatype-method"></a>Método ISampleGrabber:: SetMediaType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaType` método especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pType* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica o tipo de mídia necessário. Não é necessário definir todos os membros da estrutura; consulte comentários para obter detalhes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Por padrão, o exemplo de apoio não tem nenhum tipo de mídia preferencial. Para garantir que o exemplo de apoio se conecte ao filtro correto, chame esse método antes de criar o grafo de filtro.

Esse método restringe o intervalo de tipos de mídia que o filtro aceitará. Quando o filtro se conecta, ele tenta corresponder ao tipo de mídia fornecido em *pType*. Para fazer isso, ele compara o tipo principal, subtipo e os GUIDs de tipo de formato, nessa ordem. Para cada um desses GUIDs, se *pType* tiver o valor GUID \_ NULL, o exemplo de apoio aceitará o tipo de mídia sem nenhuma verificação adicional. Se *pType* tiver qualquer outro valor, o exemplo de apoio o comparará ao GUID no tipo de conexão. A menos que os dois GUIDs correspondam exatamente, o exemplo de apoio rejeita a conexão.

Para tipos de mídia de vídeo, o exemplo de apoio ignora o bloco de formato. Portanto, ele aceitará qualquer tamanho de vídeo e taxa de quadros. Ao chamar `SetMediaType` , defina o bloco de formato (**pbFormat**) como **nulo** e o tamanho (**cbFormat**) como zero. Para tipos de mídia de áudio, o exemplo de apoio examinará a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e exigirá que o outro filtro se conecte com esse formato — a menos que o bloco de formato em *pType* seja **nulo** ou a marca de formato seja o \_ formato Wave \_ PCM e os outros membros da estrutura sejam zero.

Exemplo 1:

-   Tipo principal: vídeo de MEDIATYPE \_
-   Subtipo: GUID \_ NULL
-   Tipo de formato: GUID \_ NULL

O exemplo de apoio aceitará qualquer tipo de vídeo em que o tipo principal é igual ao vídeo de MEDIATYPE \_ . Ele não verificará o subtipo.

Exemplo 2:

-   Tipo principal: vídeo de MEDIATYPE \_
-   Subtipo: MEDIASUBTYPE \_ RGB24
-   Tipo de formato: GUID \_ NULL

Agora, o exemplo de apoio verificará o subtipo e aceitará apenas vídeo RGB 24.

**Limitações:** Independentemente do tipo que você definir, o filtro de apoio de exemplo rejeita todos os tipos de vídeo com orientação superior ( *monoheight*) ou com um tipo de formato de formato \_ VideoInfo2. Nesse caso, embora o `SetMediaType` método tenha sucesso, o filtro não se conectará.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 
