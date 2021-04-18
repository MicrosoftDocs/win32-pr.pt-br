---
title: Método IConfigAsfWriter GetCurrentProfileId
description: O método GetCurrentProfileId recupera a ID do perfil atual. (Somente para perfis do Windows Media Format 4,0.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Formato de mídia do Windows do método GetCurrentProfileId
- Método GetCurrentProfileId Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105781630"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>Método IConfigAsfWriter:: GetCurrentProfileId

O método **GetCurrentProfileId** recupera a ID do perfil atual. (Somente para perfis do Windows Media Format 4,0.)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwProfileId* \[ fora\]
</dt> <dd>

Ponteiro para uma variável do tipo **DWORD** que recebe a ID do perfil atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Este método agora é obsoleto porque ele pressupõe os perfis do SDK do Windows Media Format versão 4,0. Use [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) ou [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) em vez de identificar corretamente um perfil para a versão 7,0 e posterior.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 