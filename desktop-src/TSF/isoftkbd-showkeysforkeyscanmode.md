---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc.h)
description: O método ISoftKbd ShowKeysForKeyScanMode exibe as chaves usadas para o modo de verificação de tecla para um teclado suave.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Método ShowKeysForKeyScanMode Estrutura de Serviços de Texto
- Método ShowKeysForKeyScanMode Estrutura de Serviços de Texto interface , ISoftKbd
- Interface ISoftKbd Estrutura de Serviços de Texto , método ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844c9f39529e1a66437c83672acc8b2d3ad2a3e3ff3a1ad31c4d9bd97248d010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877268"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>Método ISoftKbd::ShowKeysForKeyScanMode

O **método ISoftKbd::ShowKeysForKeyScanMode** exibe as chaves usadas para o modo de verificação de tecla para um teclado soft.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpKeyID* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de elementos KEYID indicando os identificadores de chaves a exibir.

</dd> <dt>

*iKeyNum* \[ Em\]
</dt> <dd>

O número de chaves a exibir.

</dd> <dt>

*fHighL* \[ Em\]
</dt> <dd>

TRUE se o método for realçar as chaves e **FALSE** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um dos parâmetros é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





