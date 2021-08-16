---
description: Sugere a política de segurança a ser aplicada ao navegador.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Método IItemPreviewerExt:: SuggestBrowserPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 84446b49ab723f161de8f148e95916202efe06176191e820ab8bafc88ed9158a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969755"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>Método IItemPreviewerExt:: SuggestBrowserPolicy

Sugere a política de segurança a ser aplicada ao navegador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwContext* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O identificador de contexto para a operação. Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \***

Um ponteiro para um valor DWORD que contém sinalizadores de verificação de verificação. O sinalizador de **\_ \_ conteúdo não confiável do BROWSERPOLICY** desabilita qualquer possibilidade de a visualização ser capaz de executar script ou ActiveX. O parâmetro *pdwFlags* não deve ser um ponteiro **nulo** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.

para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**linkid**](-search-linktype.md) .

O uso do sinalizador de **\_ \_ conteúdo não confiável BROWSERPOLICY** é altamente recomendável para desabilitar qualquer possibilidade da visualização ser capaz de executar script ou ActiveX. O método **IItemPreviewerExt:: SuggestBrowserPolicy** pode retornar informações sobre se o item que está sendo visualizado é confiável ou não. isso permitirá que o controle trident do previsor execute o script e até mesmo ActiveX controles. Como o pré-visor geralmente usa arquivos temporários para gerar a visualização, fazer isso pode resultar em execução de código e script inesperado na zona do computador local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




