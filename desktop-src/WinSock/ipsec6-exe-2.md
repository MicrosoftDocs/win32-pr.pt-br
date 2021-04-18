---
description: A configuração de políticas IPSec e associações de segurança para IPv6 é feita com Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764264"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

A configuração de políticas IPSec e associações de segurança para IPv6 é feita com Ipsec6.exe. A seguir estão Ipsec6.exe subcomandos:

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**Ipsec6 SP \[** _Interface_ do *_\]_*
</dt> <dd>

Exibe as políticas de segurança ativas. Como alternativa, exibe as políticas de segurança ativas para uma interface específica.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**Ipsec6 SA**
</dt> <dd>

Exibe associações de segurança ativas.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 c \[** _Nome do arquivo (sem extensão)_*_\]_*
</dt> <dd>

Cria arquivos usados para configurar as associações de segurança e política de segurança. Cria *filename*. SPD para políticas de segurança e *filename*. sad para associações de segurança. Use os arquivos criados como modelos para configurar políticas de segurança ou associações de segurança. Os arquivos podem ser modificados com um editor de texto. Para invocar a configuração contida nos arquivos SPD e SAD, use o comando **Ipsec6 a** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 a \[** _Nome do arquivo (sem extensão)_*_\]_*
</dt> <dd>

Adiciona políticas de segurança em *filename*. SPD e associações de segurança em *filename*. sad à lista de políticas de segurança ativas e associações de segurança.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 i \[**  *_\] \[_* _Nome de arquivo da política (sem extensão)_*_\]_*
</dt> <dd>

Adiciona políticas de segurança em *filename*. SPD e associações de segurança em *filename*. sad à lista de políticas de segurança ativas e associações de segurança, conforme referenciado pelo número da política.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**Ipsec6 d \[ Type = SP SA \] \[** _IndexNumber_*_\]_*
</dt> <dd>

Exclui políticas de segurança ou associações de segurança da lista de políticas de segurança ativas e associações de segurança, conforme referenciado pelo seu número de índice (exibido com **Ipsec6 SP** ou **Ipsec6 SA**).

</dd> </dl>

 

 



