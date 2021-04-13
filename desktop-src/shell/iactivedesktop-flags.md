---
description: Esta seção descreve os sinalizadores usados pelos métodos de interface IActiveDesktop.
title: Sinalizadores IActiveDesktop (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968786"
---
# <a name="iactivedesktop-flags"></a>Sinalizadores de IActiveDesktop

Esta seção descreve os sinalizadores usados pelos métodos de interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**\_aplicar \_ tudo ao AD**
</dt> <dd> <dl> <dt>



Agregação de * * * * AD \_ Apply \_ salvar * * * *, * * * * AD \_ Apply \_ HTMLGEN * * * * e * * * * AD \_ aplicam a \_ atualização * * * * * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ aplicar \_ atualização em buffer \_**
</dt> <dd> <dl> <dt>



Inicia um temporizador e agrega todas as solicitações de atualização feitas com esse sinalizador durante esse intervalo de tempo em uma única atualização. Esse intervalo é definido em cinco segundos. No final do intervalo, ou se uma atualização for solicitada durante o intervalo sem um * * * * * \_ o anúncio aplicar \_ \_ atualização em buffer * * * * sinalizador, a atualização será feita e o temporizador será interrompido. Esse sinalizador deve ser combinado com o sinalizador * * * * AD \_ aplicar \_ atualização * * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**\_DYNAMICREFRESH de aplicação ad \_**
</dt> <dd> <dl> <dt>



[Versão 5,0](versions.md). Use HTML dinâmico para atualizar somente os itens que foram alterados desde a última atualização, não a área de trabalho inteira.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_força de aplicação do AD \_**
</dt> <dd> <dl> <dt>



Forçar uma alteração no Active Desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**\_HTMLGEN de aplicação ad \_**
</dt> <dd> <dl> <dt>



Gere novamente o arquivo HTML da área de trabalho.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_aplicar \_ atualização do AD**
</dt> <dd> <dl> <dt>



Atualize o item da área de trabalho.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_aplicar \_ salvamento de AD**
</dt> <dd> <dl> <dt>



Salve o item da área de trabalho.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ tudo**
</dt> <dd> <dl> <dt>



Agregação dos \_ valores elem de comp \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ elem \_ verificado**
</dt> <dd> <dl> <dt>



O item foi verificado.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ elem \_ CURITEMSTATE**
</dt> <dd> <dl> <dt>



O estado atual do item da área de trabalho.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ elem \_ FriendlyName**
</dt> <dd> <dl> <dt>



O nome amigável do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem \_ NoScroll**
</dt> <dd> <dl> <dt>



O item não é rolável.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ elem \_ original do \_ CSI**
</dt> <dd> <dl> <dt>



As informações do estado do item da área de trabalho original.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ elem \_ pos \_ esquerdo**
</dt> <dd> <dl> <dt>



A posição horizontal do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ pos \_ superior**
</dt> <dd> <dl> <dt>



A posição vertical do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ elem \_ pos \_ ZINDEX**
</dt> <dd> <dl> <dt>



O índice z do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ restaurou o \_ CSI**
</dt> <dd> <dl> <dt>



As informações de estado do item da área de trabalho restaurado.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**altura do tamanho da COMP \_ elem \_ \_**
</dt> <dd> <dl> <dt>



A altura do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**largura do tamanho da COMP \_ elem \_ \_**
</dt> <dd> <dl> <dt>



A largura do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**origem do COMP \_ elem \_**
</dt> <dd> <dl> <dt>



A origem original do item.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_tipo de elem de comp \_**
</dt> <dd> <dl> <dt>



O tipo do item.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**tipo de COMP \_ \_ CFHTML**
</dt> <dd> <dl> <dt>



HTML de formato compactado.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_controle de tipo de comp \_**
</dt> <dd> <dl> <dt>



O item é um controle.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**tipo de COMP \_ \_ HTMLDOC**
</dt> <dd> <dl> <dt>



O item é um documento HTML. Esse sinalizador só deve ser usado quando absolutamente necessário. Ele faz com que um documento HTML seja inserido literalmente no arquivo desktop. htt usado para controlar o layout da área de trabalho. Na maioria dos casos, você deve usar o sinalizador * * * * tipo de COMP do \_ \_ site * * * * para adicionar itens à área de trabalho.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**tipo de COMP \_ \_ Max**
</dt> <dd> <dl> <dt>



O valor máximo de um sinalizador de tipo de COMP \_ \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_imagem do tipo comp \_**
</dt> <dd> <dl> <dt>



O item é uma imagem.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**tipo de COMP \_ \_ site**
</dt> <dd> <dl> <dt>



O item é um site.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_parte superior do componente**
</dt> <dd> <dl> <dt>



Um valor de ordem z que significa que o item está na parte superior.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE \_ Center**
</dt> <dd> <dl> <dt>



O papel de parede está centralizado.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**
</dt> <dd> <dl> <dt>



O valor máximo de um \_ \* sinalizador WPSTYLE.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**
</dt> <dd> <dl> <dt>



O papel de parede é alongado para se ajustar à tela inteira.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**bloco do WPSTYLE \_**
</dt> <dd> <dl> <dt>



O papel de parede é enlado.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ span**
</dt> <dd> <dl> <dt>



**Windows 8 e posterior**: o papel de parede abrange vários monitores.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
