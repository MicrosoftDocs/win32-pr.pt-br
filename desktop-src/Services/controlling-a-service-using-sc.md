---
description: 'O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:'
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlando um serviço usando SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755948"
---
# <a name="controlling-a-service-using-sc"></a>Controlando um serviço usando SC

O SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para controlar um serviço. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:

## <a name="syntax"></a>Syntax

**SC** \[ *Nome do Server* \] *Comando* \[ *ServiceName* \] \[  \] opção 1 \[ *opção 2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*
</dt> <dd>

Nome do servidor opcional. Use o formulário \\ \\ *nomedoservidor*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Linha*
</dt> <dd>

Um dos seguintes comandos:

<dl> <dd>continue</dd> <dd>controle</dd> <dd>interrogar</dd> <dd>pause</dd> <dd>iniciar</dd> <dd>parar</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*
</dt> <dd>

O nome do serviço, conforme especificado quando ele foi instalado.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*opção 1*
</dt> <dd>

Um parâmetro opcional.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*opção 2*
</dt> <dd>

Um parâmetro opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para ver a sintaxe completa de um comando, use o seguinte comando:

 *comando* SC

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitações de controle de serviço](service-control-requests.md)
</dt> <dt>

[Inicialização do serviço](service-startup.md)
</dt> </dl>

 

 



