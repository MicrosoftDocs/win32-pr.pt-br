---
title: Método IConfigAsfWriter GetCurrentProfileGuid
description: O método GetCurrentProfileGuid recupera o GUID atual Windows perfil do sistema de mídia.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Formato de mídia do windows do método GetCurrentProfileGuid
- Método GetCurrentProfileGuid windows Formato de Mídia, interface IConfigAsfWriter
- Formato de mídia da interface IConfigAsfWriter , método GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433635"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Método IConfigAsfWriter::GetCurrentProfileGuid

O **método GetCurrentProfileGuid** recupera o GUID atual Windows perfil do sistema de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProfileGuid* \[ out\]
</dt> <dd>

Ponteiro para uma variável do **tipo GUID** que identifica o perfil do sistema atual que está sendo usado pelo filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método não é usado com perfis personalizados (incluindo todos os perfis que incluem fluxos que usam os codecs de Áudio de Mídia e Vídeo do Windows) porque todos esses perfis são criados por aplicativos e não têm nenhum identificador guid. Se nenhum perfil do sistema for carregado, *pProfileGuid* será definido como **NULL.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 