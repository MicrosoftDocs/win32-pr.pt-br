---
description: Inicializa o filtro. chamado pelo WIA (Windows image Acquisition) 2,0 antes do download de cada imagem.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Método IWiaImageFilter:: InitializeFilter (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 43b818c3adc9926c4ba27f11f5d489ffc0b97e4443d0427e7a12067e9062072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440441"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Método IWiaImageFilter:: InitializeFilter

Inicializa o filtro. chamado pelo WIA (Windows image Acquisition) 2,0 antes do download de cada imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaItem2* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) que representa a imagem de visualização.

</dd> <dt>

*pWiaTransferCallback* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Especifica um ponteiro para a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) do aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando um aplicativo chama [**Download**](-wia-iwiatransfer-download.md) e quando um aplicativo chama a função do componente de visualização do WIA 2,0 `GetNewPreview` . **IWiaImageFilter:: InitializeFilter** armazena as referências a *pWiaItem2* e *pWiaTransferCallback* para passar nessas funções. Esses dois ponteiros de interface devem ser armazenados como variáveis de membro e [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve ser chamado para cada um. Os ponteiros de interface também são necessários na implementação do filtro de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) e [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante a aquisição da imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
