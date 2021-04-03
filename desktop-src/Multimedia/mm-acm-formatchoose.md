---
title: Mensagem de MM_ACM_FORMATCHOOSE (MSACM. h)
description: A \_ mensagem mm ACM \_ FORMATCHOOSE notifica uma função de gancho de caixa de diálogo acmFormatChoose antes de adicionar um elemento a uma das três caixas de listagem suspensas.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- Multimídia do Windows de mensagem MM_ACM_FORMATCHOOSE
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645255"
---
# <a name="mm_acm_formatchoose-message"></a>\_Mensagem mm ACM \_ FORMATCHOOSE

A mensagem **mm \_ ACM \_ FORMATCHOOSE** notifica uma função de gancho de caixa de diálogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) antes de adicionar um elemento a uma das três caixas de listagem suspensas. Essa mensagem permite que um aplicativo Personalize ainda mais as seleções disponíveis por meio da interface do usuário.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Caixa de listagem suspensa sendo inicializada e uma operação de verificação ou adição.



| Requisito | Valor |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATCHOOSE \_ de \_ verificação personalizada    | O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a ser adicionada à caixa de listagem suspensa nome personalizado.                                                                                                   |
| \_Adicionar formato \_ FORMATCHOOSE       | O parâmetro *lParam* é um ponteiro para um buffer que aceitará que uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) seja adicionada à caixa de listagem suspensa formato. O aplicativo deve copiar a estrutura de formato a ser adicionada a esse buffer. |
| \_verificação de formato de FORMATCHOOSE \_    | O parâmetro *lParam* é um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a ser adicionada à caixa de listagem suspensa formato.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ Add    | O parâmetro *lParam* é um ponteiro para uma variável que aceitará que uma marca de formato de onda-áudio seja adicionada à caixa de listagem suspensa de marca de formato.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ Verify | O parâmetro *lParam* é uma marca de formato de áudio de forma de onda a ser listada na caixa de listagem suspensa Formatar marca.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido pela caixa de listagem especificada no parâmetro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se um aplicativo tratar essa mensagem ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o aplicativo processar a \_ operação de adição de formato FILTERCHOOSE \_ , o tamanho do buffer de memória fornecido em *lParam* será determinado da função [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Se seu aplicativo estiver processando uma operação de verificação, ele poderá impedir que a caixa de diálogo liste essa seleção chamando a função **SetWindowLong** com *NINDEX* definida como DWL \_ MSGRESULT e *lNewLong* definida como **false** (conversão para um tipo de dados **Long** ). Para permitir que a caixa de diálogo liste essa seleção, chame essa função com *lNewLong* definido como **true**.

Se seu aplicativo estiver processando uma operação de adição, ele poderá indicar que não é necessária mais adições chamando a função **SetWindowLong** com *NINDEX* definido como DWL \_ MSGRESULT e *lNewLong* definida como **false** (conversão para um tipo de dados **Long** ). Para indicar que mais adições são necessárias, chame essa função com *lNewLong* definido como **true**.

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

 

