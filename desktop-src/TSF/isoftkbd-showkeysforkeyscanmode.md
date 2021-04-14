---
title: Método ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: O método ISoftKbd ShowKeysForKeyScanMode exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Estrutura de serviços de texto do método ShowKeysForKeyScanMode
- Método ShowKeysForKeyScanMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método ShowKeysForKeyScanMode
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
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455642"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>Método ISoftKbd:: ShowKeysForKeyScanMode

O método **ISoftKbd:: ShowKeysForKeyScanMode** exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.

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

*lpKeyID* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de elementos KEYID que indica os identificadores de chaves a serem exibidos.

</dd> <dt>

*iKeyNum* \[ no\]
</dt> <dd>

O número de chaves a serem exibidas.

</dd> <dt>

*fHighL* \[ no\]
</dt> <dd>

TRUE se o método for realçar as chaves; caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





