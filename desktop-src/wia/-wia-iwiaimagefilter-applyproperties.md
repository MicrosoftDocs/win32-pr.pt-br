---
description: Permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Método IWiaImageFilter:: Applyproperties (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768387"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>Método IWiaImageFilter:: Applyproperties

Permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaPropertyStorage* \[ no\]
</dt> <dd>

Tipo: **[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

Especifica um ponteiro para o [_ *IWiaPropertyStorage* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para as propriedades a serem aplicadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Não chame esse método diretamente do seu aplicativo. Ele é chamado pela aquisição de imagem do Windows (WIA) 2,0 depois que o filtro de processamento de imagem processou os dados brutos.

*pWiaPropertyStorage* é a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) na qual o filtro de processamento de imagem deve gravar propriedades. Um filtro de processamento de imagem deve usar apenas o método [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) para gravar propriedades.

Esse método permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo). Isso pode ser necessário para filtros que implementam recursos como a exposição automática durante a verificação de filmes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
