---
description: Especifique os níveis de proteção para o sistema de gerenciamento de geração de cópia&\# 8212; Analógico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-um sinalizador de proteção (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370544"
---
# <a name="cgms-a-protection-flags"></a>CGMS-um sinalizador de proteção

As constantes na tabela a seguir especificam os níveis de proteção para o sistema de gerenciamento de geração de cópia analógica (CGMS-A).



| Constante/valor                                                                                                                                                                                                                                                                                                 | Descrição                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_ off**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A está desabilitada. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ CGMSA de \_ cópia \_ gratuita**</dt> <dt></dt> </dl>                                                              | O nível de proteção é cópia livre.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ CGMSA \_ copiar \_ não \_ mais**</dt> <dt>0x02</dt> </dl>                                                          | O nível de proteção não é mais. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ CGMSA \_ copiar \_ uma \_**</dt> <dt>0x03</dt> de geração </dl>                                     | O nível de proteção é cópia de uma geração. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ \_Cópia CGMSA \_ nunca**</dt> <dt>0x04</dt> </dl>                                                                 | O nível de proteção nunca é cópia.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ \_Controle de redistribuição CGMSA \_ \_ necessário**</dt> <dt>0x08</dt> </dl> | É necessário o controle de redistribuição (também chamado de *sinalizador de difusão*). Esse sinalizador pode ser combinado com os outros sinalizadores.<br/> |



## <a name="remarks"></a>Comentários

Esses sinalizadores são equivalentes às constantes de enumeração de **\_ nível de \_ proteção \_ Copp CGMSA** usadas no protocolo Copp (certificado de proteção de saída).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




