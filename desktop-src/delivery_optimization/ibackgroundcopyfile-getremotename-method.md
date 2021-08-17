---
title: Método getremotename IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera o nome remoto do arquivo.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Método getremotename
- Método getremotename, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, método getremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810321"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>Método IBackgroundCopyFile:: getremotename

Recupera o nome remoto do arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppName* \[ fora\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome remoto do arquivo a ser transferido. O nome é totalmente qualificado. Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.

## <a name="remarks"></a>Comentários

Para alterar o nome do arquivo remoto, chame o método [**IBackgroundCopyFile2:: Setremotoname**](ibackgroundcopyfile2-setremotename-method.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile:: getlocalname**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

