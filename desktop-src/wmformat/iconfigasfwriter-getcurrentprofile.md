---
title: Método GetCurrentProfile de IConfigAsfWriter
description: O método GetCurrentProfile recupera o perfil definido pelo aplicativo.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Formato de mídia do windows do método GetCurrentProfile
- Formato de mídia do windows do método GetCurrentProfile, interface IConfigAsfWriter
- Formato de mídia da interface IConfigAsfWriter , método GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198377"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Método IConfigAsfWriter::GetCurrentProfile

O **método GetCurrentProfile** recupera o perfil definido pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppProfile* \[ out\]
</dt> <dd>

Endereço de um ponteiro que recebe a interface [**IWMProfile**](iwmprofile.md) do perfil definido pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="remarks"></a>Comentários

Se o método for bem-sucedido, o ponteiro **IWMProfile** que ele retorna terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 