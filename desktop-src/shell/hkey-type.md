---
description: Esses tipos de dados podem ser usados para especificar o tipo de um valor de registro.
title: Tipos de dados do registro (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104990483"
---
# <a name="registry-data-types"></a>Tipos de dados do registro

Esses tipos de dados podem ser usados para especificar o tipo de um valor de registro.



| Constante                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**\_binário reg**</dt> </dl>                                          | Dados binários em qualquer formulário.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | 32-número de bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | 64-número de bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD de valor \_ pequeno \_**</dt> </dl> | 32-número de bits no formato little-endian. Isso é equivalente a **reg \_ DWORD**.<br/> No formato little-endian, um valor multibyte é armazenado na memória do byte mais baixo (o "pequeno fim") para o byte mais alto. Por exemplo, o valor 0x12345678 é armazenado como (0x78 0x56 0x34 0x12) no formato little-endian.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWORD \_ Little \_ ENDIAN**</dt> </dl> | Um número de 64 bits no formato little-endian. Isso é equivalente a **reg \_ QWORD**. <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ Big \_ ENDIAN**</dt> </dl>          | 32-número de bits no formato big-endian.<br/> No formato big endian, um valor multibyte é armazenado na memória do byte mais alto (o "Big end") para o byte mais baixo. Por exemplo, o valor 0x12345678 é armazenado como (0x12 0x34 0x56 0x78) no formato big endian.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ expande \_ sz**</dt> </dl>                                | Cadeia de caracteres terminada em nulo que contém referências não expandidas a variáveis de ambiente (por exemplo, "% PATH%"). Será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**\_link reg**</dt> </dl>                                                | Link simbólico Unicode.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ multi \_ sz**</dt> </dl>                                   | Matriz de cadeias de caracteres terminadas em nulo que são terminadas por dois caracteres nulos.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ None**</dt> </dl>                                                | Nenhum tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**\_lista de recursos do reg \_**</dt> </dl>                    | Lista de recursos de driver de dispositivo.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG \_ sz**</dt> </dl>                                                      | Cadeia de caracteres terminada em nulo. Será uma cadeia de caracteres Unicode ou ANSI, dependendo se você usar as funções Unicode ou ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




