---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir inscrições.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Máscaras de acesso à inscrição (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870106"
---
# <a name="enlistment-access-masks"></a>Máscaras de acesso à inscrição

O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir inscrições.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informações de consulta de inscrição \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



O chamador pode consultar o KTM para obter informações sobre a inscrição.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informações do conjunto de inscrição \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



O chamador pode definir informações sobre a inscrição.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**recuperação de inscrição \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



O chamador pode recuperar uma inscrição.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_direitos subordinados à inscrição \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



O chamador pode concluir ações que um Gerenciador de recursos faz em nome da transação. A seguir está uma lista de ações:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_direitos superiores de inscrição \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



O chamador pode se inscrever na transação como um Gerenciador de transações superior.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_leitura genérica de inscrição \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ informações** **padrão de \_ \_ leitura** e consulta de inscrição.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_gravação genérica de inscrição \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de inscrição** e **\_ recuperação de inscrição**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_execução genérica de inscrição \_**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ direitos de \_ execução padrão**, **\_ recuperação de inscrição** e **\_ \_ direitos subordinados à inscrição**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**\_todos os \_ acessos à inscrição**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Esse valor define todos os bits válidos para um valor de acesso à inscrição.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




