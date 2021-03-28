---
description: Sinalizadores que restringem os dados a serem definidos ou retornados.
title: SRRF (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011176"
---
# <a name="srrf"></a>SRRF

Sinalizadores que restringem os dados a serem definidos ou retornados.



| Constante/valor                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt> </dl>                 | Digite REG \_ None.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ sz**</dt> <dt>0x00000002</dt> </dl>                       | Digite REG \_ sz. \_Os tipos reg expande \_ sz são convertidos automaticamente em reg \_ sz, a menos que o \_ sinalizador NOEXPAND SRRF seja especificado.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**SRRF \_ * \_ Reg \_ expandir \_ sz**</dt> <dt>0x00000004</dt> </dl> | Digite REG \_ expande \_ sz. Se estiver recuperando um valor, você também deverá obter o \_ sinalizador NOEXPAND SRRF ou [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) falhará com um parâmetro de erro \_ inválido \_ .<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**SRRF \_ 0x00000008 \_ de \_ binário do Reg de RT**</dt> <dt></dt> </dl>           | Digite REG \_ Binary.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt> </dl>              | Digite REG \_ DWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ multi \_ sz**</dt> <dt>0x00000020</dt> </dl>    | Digite REG \_ multi \_ sz.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**SRRF \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt> </dl>              | Digite REG \_ Qword.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | \_Tipos binários reg DWORD e 32 bits \_ . Isso é equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ \_ DWORD. Se você recuperar um valor, se os dados binários do valor forem maiores que 32 bits, ele não será retornado.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**SRRF \_ RT \_ QWORD**</dt> <dt>0x00000048</dt> </dl>                           | \_Tipos binários reg QWORD e 64-bit \_ . Isso é equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ Qword. Se você recuperar um valor, se os dados binários do valor forem maiores que 64 bits, ele não será retornado.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**SRRF \_ RT \_ qualquer**</dt> <dt>0x0000FFFF</dt> </dl>                                 | Todos os tipos. Defina esse sinalizador se nenhum outro valor de RT de SRRF \_ for definido.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**SRRF \_ RM \_ qualquer**</dt> <dt>0x00000000</dt> </dl>                                 | Nenhuma restrição de modo. Esse é o valor padrão.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**SRRF \_ 0x00010000 \_ normal do RM**</dt> <dt></dt> </dl>                        | Restrinja o modo de inicialização do sistema para "inicialização normal".<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**SRRF \_ 0x00020000 \_ seguro do RM**</dt> <dt></dt> </dl>                              | Restrinja o modo de inicialização do sistema para "modo de segurança".<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**SRRF \_ 0x00040000 RM \_ SAFENETWORK**</dt> <dt></dt> </dl>         | Restrinja o modo de inicialização do sistema para "modo de segurança com rede".<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**SRRF \_ 0x10000000 NOEXPAND**</dt> <dt></dt> </dl>                            | Não expanda automaticamente as \_ \_ cadeias de caracteres do ambiente reg Expand sz.<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt> </dl>             | Se for recuperar um valor, se *pvData* não for **nulo**, defina o conteúdo do buffer *pvData* como todos os zeros em caso de falha.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt> </dl>                                  | Ao recuperar um valor, se a chave solicitada for virtualizada, falha com o \_ arquivo de erro \_ não \_ encontrado.<br/>                                                                                                            |



## <a name="remarks"></a>Comentários

Esses valores são definidos em Shlwapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




