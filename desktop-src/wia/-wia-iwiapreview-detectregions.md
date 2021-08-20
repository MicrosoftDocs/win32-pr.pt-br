---
description: 'Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método IWiaPreview:: GetNewPreview para o filtro.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: 'IWiaPreview: método etectRegions de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3a1663c50213f959da9f6d7f450fb58a5ac0bb4e1bb9ffec8e302abd15e4698e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669462"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview: método etectRegions de:D

Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para o filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Não usado. Defina como zero (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Esse método pode retornar um desses valores.



| Código de retorno                                                                               | Descrição                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | A operação teve êxito.<br/>              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | O driver não dá suporte à segmentação.<br/> |
| <dl> <dt>**otherwise**</dt> </dl>  | Um código de erro COM padrão.<br/>                |



 

## <a name="remarks"></a>Comentários

Um aplicativo deve chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) antes de chamar essa função.

quando o componente de visualização de aquisição de imagem de Windows (WIA) 2,0 chama **IWiaPreview::D etectregions**, ele invoca o filtro de segmentação de driver e passa a interface [**IWiaItem2**](-wia-iwiaitem2.md) que foi passada anteriormente para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Ele também passa a imagem armazenada internamente em cache para o filtro. O filtro de segmentação usa a imagem armazenada em cache para criar as extensões filhas.

Se um aplicativo alterar as propriedades da interface [**IWiaItem2**](-wia-iwiaitem2.md) depois de chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), as propriedades originais deverão ser restauradas antes que o aplicativo chame **IWiaPreview::D etectregions**. Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) para restaurar as propriedades originais.

**IWiaPreview::D etectregions** é usado para determinar as "subregiãos" da imagem armazenada em cache. Para cada sub-região detectada, um novo item filho WIA 2,0 é criado na interface [**IWiaItem2**](-wia-iwiaitem2.md) . Para cada item filho, o filtro de segmentação deve definir os valores para as seguintes propriedades WIA 2,0: WIA \_ IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS XEXTENT e \_ WIA \_ IPS \_ YEXTENT. Um filtro mais avançado define outras propriedades de WIA 2,0, como \_ os IPs WIA distorção \_ \_ X e WIA IPS de \_ distorção \_ \_ Y, se o driver oferecer suporte à remoção de distorção. Os IPs \_ WIA \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ XEXTENT e \_ \_ as propriedades YEXTENT IPS WIA representam o retângulo delimitador da área a ser verificada.

O driver pode não dar suporte à segmentação. Antes de chamar **IWiaPreview::D etectregions**, um aplicativo geralmente verifica se o driver dá suporte \_ à \_ propriedade de segmentação de IPS WIA. Se a propriedade não for implementada, a segmentação não terá suporte e **IWiaPreview::D etectregions** falhará E retornará e \_ NOTIMPL.

O aplicativo deve limpar os itens filho que são criados chamando **IWiaPreview::D etectregions**. Por exemplo, se um aplicativo fizer uma chamada adicional para **IWiaPreview::D etectregions** no mesmo item, ele deverá limpar os itens filho anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




