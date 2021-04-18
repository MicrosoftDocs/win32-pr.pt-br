---
description: Esses sinalizadores especificam o comportamento do localizador de mídia.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Sinalizadores de validação de nome de arquivo (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766312"
---
# <a name="file-name-validation-flags"></a>Sinalizadores de validação de nome de arquivo

\[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

Esses sinalizadores especificam o comportamento do localizador de mídia.



| Constante/valor                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ \_Verificar VALIDATEF**</dt> <dt>0x01</dt> </dl>                   | Verifique a validade dos nomes de arquivo. Você deve definir esse sinalizador para validar nomes de arquivo. Caso contrário, os outros sinalizadores não terão nenhum efeito.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ VALIDATEF \_ Popup**</dt> <dt>0x02</dt> </dl>                   | Se um arquivo não estiver localizado, exiba uma caixa de diálogo abrir arquivo para o usuário final.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Se um arquivo ausente estiver localizado, exiba brevemente uma caixa de mensagem com o nome e o local do arquivo. Esse sinalizador é útil principalmente para fins de teste; a caixa de mensagem provavelmente não é adequada para um produto de varejo.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ VALIDATEF \_ substituir**</dt> <dt>0x08</dt> </dl>             | Se um arquivo ausente estiver localizado, atualize o nome do objeto de origem. (Válido somente no método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Sempre use um arquivo local, mesmo se houver uma versão do arquivo na rede.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt> </dl>                | Não pesquise arquivos ausentes. Os nomes de arquivo ainda serão validados se você definir o \_ sinalizador de verificação SFN VALIDATEF \_ .<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Ignorar objetos de origem sem som. (Válido somente no método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)<br/>                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




