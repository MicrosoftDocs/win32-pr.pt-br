---
title: Método IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
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
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369543"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>Método IBackgroundCopyFile2:: GetFileRanges

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

*RangeCount* \[ entrada, saída\]
</dt> <dd>

Número de elementos em *intervalos*.

</dd> <dt>

*Intervalos* \[ de fora\]
</dt> <dd>

Matriz de estruturas de [**BG_FILE_RANGE**](bg-file-range.md) que especificam os intervalos a serem baixados. Quando terminar, chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para *intervalos* gratuitos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os seguintes valores de retorno, bem como outros.



| Código de retorno                                                                              | Descrição                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Sucesso<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Nenhum intervalo foi especificado ou o trabalho é um trabalho de upload ou de resposta de upload. *RangeCount* é definido como zero e os *intervalos* são definidos como **NULL**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 é definido como 83e81b93-0873-474D-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

