---
description: 'o SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para consultar ou modificar o banco de dados dos serviços instalados. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:'
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configurando um serviço usando SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 976eb5fb8e9a462e4d1de38413593343dd1d8624985593f6ecb9c691ae9670da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968223"
---
# <a name="configuring-a-service-using-sc"></a>Configurando um serviço usando SC

o SDK do Windows contém um utilitário de linha de comando, Sc.exe, que pode ser usado para consultar ou modificar o banco de dados dos serviços instalados. Seus comandos correspondem às funções fornecidas pelo SCM. A sintaxe é a seguinte:

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

<dl> <dd>boot</dd> <dd>config</dd> <dd>create</dd> <dd>excluir</dd> <dd>descrição</dd> <dd>EnumDepend</dd> <dd>falha</dd> <dd>failureflag</dd> <dd>GetDisplayName</dd> <dd>GetKeyName</dd> <dd>Bloqueio</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>Consulta</dd> <dd>QueryEx</dd> <dd>privs</dd> <dd>QueryLock</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>sidtype</dd> </dl> </dd> <dt>

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

[Configuração de serviço](service-configuration.md)
</dt> <dt>

[Instalação, remoção e enumeração de serviço](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



