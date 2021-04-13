---
description: Obtém um ícone de dispositivo personalizado.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'Método IWiaUIExtension2:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501786"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>Método IWiaUIExtension2:: GetDeviceIcon

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

Tipo: **HICON \** _

Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.

</dd> <dt>

_nSize * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Especifica o tamanho do ícone desejado, em pixels. O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se o método for bem sucedido, ele retornará S \_ OK. Se o método falhar, ele retornará um código de erro apropriado. A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.



| Código do erro    | Descrição                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | O parâmetro bstrDeviceId ou phIcon é **nulo** ou bstrDeviceId não aponta para uma cadeia de caracteres de ID de dispositivo WIA válida |
| E \_ falha       | Nenhum recurso de ícone está disponível.                                                                               |
| E \_ NOTIMPL    | Nenhum ícone do tamanho solicitado está disponível.                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




