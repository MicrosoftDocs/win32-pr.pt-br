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
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460986"
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

Tipo: **DWORD \** _

Um ponteiro para um valor DWORD que contém sinalizadores de verificação de verificação. O sinalizador _ *BROWSERPOLICY \_ \_ conteúdo não confiável** desabilita qualquer possibilidade de a visualização ser capaz de executar script ou ActiveX. O parâmetro *pdwFlags* não deve ser um ponteiro **nulo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

O uso do sinalizador de **\_ \_ conteúdo não confiável BROWSERPOLICY** é altamente recomendável para desabilitar qualquer possibilidade da visualização ser capaz de executar script ou ActiveX. O método **IItemPreviewerExt:: SuggestBrowserPolicy** pode retornar informações sobre se o item que está sendo visualizado é confiável ou não. Isso permitirá que o controle Trident do previsor execute o script e até controles ActiveX. Como o pré-visor geralmente usa arquivos temporários para gerar a visualização, fazer isso pode resultar em execução de código e script inesperado na zona do computador local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




