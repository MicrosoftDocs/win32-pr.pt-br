---
description: Instrumentação de Gerenciamento do Windows (WMI) tem uma nova chave do registro para habilitar ou desabilitar o recurso repositório de autorestore.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Chave do registro para configuração do repositório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789263"
---
# <a name="registry-key-for-repository-configuration"></a>Chave do registro para configuração do repositório

Instrumentação de Gerenciamento do Windows (WMI) tem uma nova chave do registro para habilitar ou desabilitar o recurso repositório de autorestore. Para obter mais informações sobre como restaurar o repositório WMI, consulte [backup ou restaurar repositório WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

No Windows 7, o comportamento padrão é restaurar automaticamente um repositório de uma versão de backup se for detectada uma corrupção de repositório. O WMI fornece o valor do registro **AutoRestoreEnabled** para desabilitar esse recurso.

As chaves do registro para WMI estão localizadas no registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Permite que o usuário determine se deseja ou não usar o recurso de repositório de restauração autorestore. Por padrão, essa chave é definida como 1 e o recurso repositório de autorestore é habilitado.

As seguintes configurações são possíveis:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Desabilitado

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

habilitado

</dd> </dl> </dd> </dl>

O valor do registro **AutoRestoreEnabled** pode ser modificado usando o console de gerenciamento de política de grupo (GPMC). Para obter mais informações, consulte [console de gerenciamento de política de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Este procedimento fornece detalhes sobre como habilitar ou desabilitar o recurso repositório de autorestore:

**Para alterar o valor padrão da chave **AutoRestoreEnabled** usando política de grupo**

1.  Abra o GPMC.
2.  Crie um objeto de Política de Grupo (GPO).
3.  Edite o GPO.
4.  Navegue até preferências/configurações do Windows/registro.
5.  Clique com o botão direito do mouse e selecione **novo... Registro**. Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.
6.  Selecione o comando **Atualizar** .
7.  Selecione o seguinte caminho de chave do registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.
8.  No campo **nome** , insira **AutoRestoreEnabled**.
9.  No campo de **dados** , digite 0 para desabilitar ou 1 para habilitar o recurso repositório de autorestore.
10. Clique em OK.

 

 
