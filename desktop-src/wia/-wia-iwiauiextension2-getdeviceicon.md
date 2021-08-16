---
description: 'Método IWiaUIExtension2:: GetDeviceIcon – Obtém um ícone de dispositivo personalizado.'
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
ms.openlocfilehash: 236a12bdf37a3d4c73a4601dd35667e946442bab3fc8dc66340d5f889b165f20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669378"
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

Se o método for bem sucedido, ele retornará S \_ OK. Se o método falhar, ele retornará um código de erro apropriado. A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.



| Código do erro    | Descrição                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | O parâmetro bstrDeviceId ou phIcon é **nulo** ou bstrDeviceId não aponta para uma cadeia de caracteres de ID de dispositivo WIA válida |
| E \_ falha       | Nenhum recurso de ícone está disponível.                                                                               |
| E \_ NOTIMPL    | Nenhum ícone do tamanho solicitado está disponível.                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




