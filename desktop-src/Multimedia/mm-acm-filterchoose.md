---
title: Mensagem de MM_ACM_FILTERCHOOSE (MSACM. h)
description: A \_ mensagem mm ACM \_ FILTERCHOOSE notifica uma função de gancho da caixa de diálogo acmFilterChoose antes de adicionar um elemento a uma das três caixas de listagem suspensas.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- Multimídia do Windows de mensagem MM_ACM_FILTERCHOOSE
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085242"
---
# <a name="mm_acm_filterchoose-message"></a>\_Mensagem mm ACM \_ FILTERCHOOSE

A mensagem **mm \_ ACM \_ FILTERCHOOSE** notifica uma função de gancho da caixa de diálogo [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) antes de adicionar um elemento a uma das três caixas de listagem suspensas. Essa mensagem permite que um aplicativo Personalize ainda mais as seleções disponíveis por meio da interface do usuário.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Caixa de listagem suspensa sendo inicializada e uma operação de verificação ou adição.



| Requisito | Valor |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTERCHOOSE \_ de \_ verificação personalizada    | O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) a ser adicionada à caixa de listagem suspensa nome personalizado.                                                                                                   |
| \_Adicionar filtro \_ FILTERCHOOSE       | O parâmetro *lParam* é um ponteiro para um buffer que aceitará que uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) seja adicionada à caixa de listagem suspensa de filtro. O aplicativo deve copiar a estrutura do filtro a ser adicionada a esse buffer. |
| \_verificação de filtro FILTERCHOOSE \_    | O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) a ser adicionada à caixa de listagem suspensa de filtro.                                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ Add    | O parâmetro *lParam* é um ponteiro para um **DWORD** que aceitará que uma marca de filtro de forma de onda seja adicionada à caixa de listagem suspensa marca de filtro.                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ Verify | O parâmetro *lParam* é uma marca de filtro de onda-áudio a ser listada na caixa de listagem suspensa marca de filtro.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido pela caixa de listagem especificada no parâmetro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se um aplicativo tratar essa mensagem ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o aplicativo processar a \_ operação de adição de filtro FILTERCHOOSE \_ , o tamanho do buffer de memória fornecido em *lParam* será determinado da função [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Se o aplicativo processa uma operação de verificação, o aplicativo deve preceder o valor de retorno com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) para impedir que a caixa de diálogo liste essa seleção ou com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) para permitir que a caixa de diálogo listar essa seleção. Se estiver processando uma operação de adição, o aplicativo deverá preceder o retorno com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) para indicar que não é necessária mais adições ou com **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) se mais adições forem necessárias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>MSACM. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de áudio](audio-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de áudio](audio-compression-messages.md)
</dt> </dl>

 

 





