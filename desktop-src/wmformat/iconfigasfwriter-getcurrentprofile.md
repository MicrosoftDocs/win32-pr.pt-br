---
title: Método IConfigAsfWriter GetCurrentProfile
description: O método GetCurrentProfile recupera o perfil definido pelo aplicativo.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Formato de mídia do Windows do método GetCurrentProfile
- Método GetCurrentProfile Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105768352"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Método IConfigAsfWriter:: GetCurrentProfile

O método **GetCurrentProfile** recupera o perfil definido pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppProfile* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que recebe a interface [**IWMProfile**](iwmprofile.md) do perfil definido pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o método tiver sucesso, o ponteiro **IWMProfile** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 