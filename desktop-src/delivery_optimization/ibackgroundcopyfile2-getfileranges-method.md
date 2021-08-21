---
title: Método GetFileRanges IBackgroundCopyFile2 (Deliveryoptimization.h)
description: Recupera os intervalos que você deseja baixar do arquivo remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Método GetFileRanges
- Método GetFileRanges, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, método GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047074"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>Método IBackgroundCopyFile2::GetFileRanges

Recupera os intervalos que você deseja baixar do arquivo remoto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RangeCount* \[ in, out\]
</dt> <dd>

Número de elementos em *Intervalos*.

</dd> <dt>

*Intervalos* \[ out\]
</dt> <dd>

Matriz de [**BG_FILE_RANGE**](bg-file-range.md) estruturas que especificam os intervalos a baixar. Quando terminar, chame a [**função CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *Intervalos*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes valores de retorno, bem como outros.



| Código de retorno                                                                              | Descrição                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Êxito<br/>                                                                                                                            |
| <dl> <dt>**S_false**</dt> </dl>  | Nenhum intervalo foi especificado ou o trabalho é um trabalho de upload ou upload-reply. *RangeCount* é definido como zero *e Ranges* é definido como **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 é definido como 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

