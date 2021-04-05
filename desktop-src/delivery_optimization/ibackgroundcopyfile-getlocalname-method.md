---
title: Método getlocalname IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera o nome local do arquivo.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Método getlocalname
- Método getlocalname, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, método getlocalname
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009283"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>Método IBackgroundCopyFile:: getlocalname

Recupera o nome local do arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppName* \[ fora\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no cliente. O nome é totalmente qualificado. Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile:: getremotename**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

