---
description: O Windows SDK contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlando um serviço usando SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126446"
---
# <a name="controlling-a-service-using-sc"></a>Controlando um serviço usando SC

O Windows SDK contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte.

## <a name="syntax"></a>Syntax

**sc** \[ *ServerName* \] *Comando* \[ *ServiceName* \] \[ *option1* \] \[ *option2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Servername*
</dt> <dd>

Nome do servidor opcional. Use o formato \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*
</dt> <dd>

Um dos seguintes comandos:

<dl> <dd>continue</dd> <dd>controle</dd> <dd>Interrogar</dd> <dd>pause</dd> <dd>start</dd> <dd>parar</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Servicename*
</dt> <dd>

O nome do serviço, conforme especificado quando ele foi instalado.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*option1*
</dt> <dd>

Um parâmetro opcional.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*option2*
</dt> <dd>

Um parâmetro opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para ver a sintaxe completa de um comando, use o seguinte comando:

**Comando sc** 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitações de controle de serviço](service-control-requests.md)
</dt> <dt>

[Inicialização do serviço](service-startup.md)
</dt> </dl>

 

 



