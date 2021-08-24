---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de recursos.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Máscaras de acesso do Gerenciador de recursos (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ede54d5d49533e70aa9cda2d9c4a363d61f1fdbd894108a5b83f2c5e9efc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146479"
---
# <a name="resource-manager-access-masks"></a>Máscaras de acesso do Gerenciador de recursos

O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de recursos.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_informações de consulta de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador pode consultar as informações do Gerenciador de recursos (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informações do conjunto de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador pode definir as informações do RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**recuperação de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador pode recuperar o RM especificado.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**inscrição de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador pode inscrever um RM em uma transação.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notificação de obtenção de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador pode receber uma notificação para um RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_leitura genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador tem os seguintes privilégios: \_ leitura de direitos padrão \_ , informações de consulta de ResourceManager \_ \_ e recuperação de ResourceManager \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_gravação genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador tem os seguintes privilégios: \_ gravação de direitos padrão \_ , informações do conjunto de ResourceManager \_ \_ , \_ inscrição de ResourceManager e notificação de obtenção de ResourceManager \_ \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_execução genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



O chamador tem os seguintes privilégios: \_ execução de direitos padrão \_ , \_ inscrição de ResourceManager e \_ notificação de obtenção de ResourceManager \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_todos os \_ acessos do RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



O chamador tem o seguinte privilégio: \_ direitos padrão \_ necessários.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




