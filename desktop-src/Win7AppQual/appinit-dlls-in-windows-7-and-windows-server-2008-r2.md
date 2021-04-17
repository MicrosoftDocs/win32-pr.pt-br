---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797534"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>AppInit \_ DLLs no Windows 7 e no Windows Server 2008 R2

## <a name="platform"></a>Plataforma

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

AppInit \_ DLLs é um mecanismo que permite que uma lista arbitrária de DLLs seja carregada em cada processo de modo de usuário no sistema. A Microsoft está modificando a instalação do AppInit DLLs no Windows 7 e no Windows Server 2008 R2 para adicionar um novo requisito de assinatura de código. Isso ajudará a melhorar a confiabilidade e o desempenho do sistema, além de melhorar a visibilidade da origem do software.

## <a name="configuration"></a>Configuração

Valores armazenados em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key no registro determinam o comportamento da infraestrutura AppInit \_ DLLs. A tabela a seguir descreve esses valores de registro:



<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
<th>Valores de exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {remover} $<br />
</td>
<td rowspan="2">Habilita ou desabilita globalmente AppInit_DLLs. $ {REMOVE} $<br />
</td>
<td>0x0 – AppInit_DLLs estão desabilitadas.</td>
</tr>
<tr class="even">
<td>0x1 – AppInit_DLLs estão habilitados.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Espaço ou lista delimitada por vírgulas de DLLs a serem carregadas. O caminho completo para a DLL deve ser especificado usando nomes curtos.</td>
<td>C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {remover} $<br />
</td>
<td rowspan="2">Carregar somente DLLs assinadas por código. $ {REMOVE} $<br />
</td>
<td>0x0 – carregar qualquer DLL.</td>
</tr>
<tr class="odd">
<td>0x1 – carregar somente DLLs assinadas por código.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Todas as DLLs que são carregadas pela \_ infraestrutura AppInit DLLs devem ser assinadas por código. Nos interesses da compatibilidade de aplicativos, o sistema operacional Windows 7 carregará todas as DLLs AppInit. No entanto, a Microsoft recomenda que todos os desenvolvedores de aplicativos codifiquem suas DLLs para ajudar a melhorar a confiabilidade do Windows e se preparar para a imposição de assinatura de código em versões futuras do Windows. A \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor no Windows 7 é definido como 0 por padrão.

**Windows Server 2008 R2**

Todas as DLLs que são carregadas pela \_ infraestrutura de DLLs AppInit devem ser assinadas por código. A \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor no Windows Server 2008 R2 é definido como 1 por padrão.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[AppInit DLLs no Windows 7 e no Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
