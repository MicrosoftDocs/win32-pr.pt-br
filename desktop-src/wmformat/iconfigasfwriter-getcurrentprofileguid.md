---
title: Método IConfigAsfWriter GetCurrentProfileGuid
description: O método GetCurrentProfileGuid recupera o GUID de perfil do sistema de mídia do Windows atual.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Formato de mídia do Windows do método GetCurrentProfileGuid
- Método GetCurrentProfileGuid Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294390"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Método IConfigAsfWriter:: GetCurrentProfileGuid

O método **GetCurrentProfileGuid** recupera o GUID de perfil do sistema de mídia do Windows atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProfileGuid* \[ fora\]
</dt> <dd>

Ponteiro para uma variável do tipo **GUID** que identifica o perfil do sistema atual que está sendo usado pelo filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método não é usado com perfis personalizados (incluindo todos os perfis que incluem fluxos que usam os codecs de áudio e vídeo do Windows Media), pois todos esses perfis são criados por aplicativos e não têm nenhum identificador GUID. Se nenhum perfil do sistema for carregado, *pProfileGuid* será definido como **nulo**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 