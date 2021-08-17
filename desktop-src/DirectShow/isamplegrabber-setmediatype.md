---
description: O método SetMediaType especifica o tipo de mídia para a conexão no pino de entrada do Sample Grabber.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: Método ISampleGrabber::SetMediaType (Qedit.h)
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
ms.openlocfilehash: 060ff0cc10fed441fdb2d6f2bf1bd0e66f3e8b9facec3cb52d8f270b350b1f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817697"
---
# <a name="isamplegrabbersetmediatype-method"></a>Método ISampleGrabber::SetMediaType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaType` método especifica o tipo de mídia para a conexão no pino de entrada do Sample Grabber.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ptype* 
</dt> <dd>

Ponteiro para uma [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica o tipo de mídia necessário. Não é necessário definir todos os membros da estrutura; consulte Comentários para obter detalhes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Por padrão, o Sample Grabber não tem nenhum tipo de mídia preferencial. Para garantir que o Sample Grabber se conecte ao filtro correto, chame esse método antes de criar o grafo de filtro.

Esse método restringe o intervalo de tipos de mídia que o filtro aceitará. Quando o filtro se conecta, ele tenta corresponder ao tipo de mídia dado em *pType*. Para fazer isso, ele compara os GUIDs de tipo principal, subtipo e formato, nessa ordem. Para cada um desses GUIDs, se *pType* tiver o valor GUID NULL, o Sample Grabber aceitará o tipo de mídia \_ sem nenhuma verificação posterior. Se *pType* tiver qualquer outro valor, o Sample Grabber o comparará com o GUID no tipo de conexão. A menos que os dois GUIDs corresponderem exatamente, o Sample Grabber rejeitará a conexão.

Para tipos de mídia de vídeo, o Grabber de Exemplo ignora o bloco de formato. Portanto, ele aceitará qualquer tamanho de vídeo e taxa de quadros. Quando você chama `SetMediaType` , de definido o bloco de formato (**pbFormat**) como **NULL** e o tamanho (**cbFormat**) como zero. Para tipos de mídia de áudio, o Sample Grabber examinará a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e exigirá que o outro filtro se conecte a esse formato , a menos que o bloco de formato em *pType* seja **NULL** ou a marca de formato seja WAVE FORMAT PCM e os outros membros da estrutura \_ sejam \_ zero.

Exemplo 1:

-   Tipo principal: Vídeo \_ MEDIATYPE
-   Subtipo: GUID \_ NULL
-   Tipo de formato: GUID \_ NULL

O Sample Grabber aceitará qualquer tipo de vídeo em que o tipo principal for igual a MEDIATYPE \_ Video. Ele não verificará o subtipo.

Exemplo 2:

-   Tipo principal: Vídeo \_ MEDIATYPE
-   Subtipo: MEDIASUBTYPE \_ RGB24
-   Tipo de formato: GUID \_ NULL

Agora, o Sample Grabber verificará o subtipo e aceitará apenas o vídeo RGB 24.

**Limitações:** Independentemente do tipo definido, o Filtro de Captura de Exemplo rejeita todos os tipos de vídeo com orientação de cima para baixo *(biHeight* negativo) ou com um tipo de formato FORMAT \_ VideoInfo2. Nesse caso, embora o `SetMediaType` método seja bem-sucedido, o filtro não se conectará.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o exemplo de grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber Interface**](isamplegrabber.md)
</dt> </dl>

 

 
