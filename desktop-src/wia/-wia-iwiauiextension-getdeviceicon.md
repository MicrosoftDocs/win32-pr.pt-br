---
description: 'Método IWiaUIExtension:: GetDeviceIcon – Obtém um ícone de dispositivo personalizado.'
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Método IWiaUIExtension:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116654"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Método IWiaUIExtension:: GetDeviceIcon

Obtém um ícone de dispositivo personalizado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceId* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.

</dd> <dt>

*phIcon* \[ fora\]
</dt> <dd>

Tipo: **HICON \***

Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.

</dd> <dt>

*nSize* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Especifica o tamanho do ícone desejado, em pixels. O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




