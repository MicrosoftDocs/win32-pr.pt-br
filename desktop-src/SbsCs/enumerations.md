---
description: Saiba mais sobre as enumerações usadas na API de assembly lado a lado, como ASM_CMP_FLAGS e CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Enumerações de assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a7aee5c64209176ce0690c0a9e7954ad51160a0723c1ec5d1e7e4cee5dba1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142209"
---
# <a name="side-by-side-assembly-enumerations"></a>Enumerações de assembly lado a lado

A API de assembly lado a lado usa as enumerações a seguir.



| Enumeração                                                         | Descrição                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SINALIZADORES \_ CMP DO ASM \_**](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | Usado pelo método [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) para especificar quais partes de dois nomes de assembly devem ser comparadas.                                                                       |
| [**SINALIZADORES DE \_ EXIBIÇÃO DO ASM \_**](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | Usado pelo método [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) para especificar quais partes do nome do assembly lado a lado incluir na representação de cadeia de caracteres do nome. |
| [**NOME \_ DO ASM**](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | IDs de propriedade para os pares nome-valor em um nome de assembly lado a lado.                                                                                                                    |
| [**CRIAR \_ SINALIZADORES \_ OBJ DE \_ NOME \_ ASM**](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | Usado pela [**função CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) para especificar o nome do assembly lado a lado.                                                               |



 

 

 



