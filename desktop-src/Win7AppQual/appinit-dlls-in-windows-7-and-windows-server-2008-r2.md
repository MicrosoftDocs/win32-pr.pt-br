---
description: AppInit_DLLs no Windows 7 e no Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8741039952b0ea15d32b19bc48d4197ea13751bc492ff82fc8e67b1662d0b682
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031065"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>AppInit \_ DLLs no Windows 7 e Windows Server 2008 R2

## <a name="platform"></a>Plataforma

**clientes** -Windows 7  
**servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

AppInit \_ DLLs é um mecanismo que permite que uma lista arbitrária de DLLs seja carregada em cada processo de modo de usuário no sistema. a Microsoft está modificando a instalação do AppInit DLLs no Windows 7 e no Windows Server 2008 R2 para adicionar um novo requisito de assinatura de código. Isso ajudará a melhorar a confiabilidade e o desempenho do sistema, além de melhorar a visibilidade da origem do software.

## <a name="configuration"></a>Configuração

valores armazenados sob a \_ chave HKEY LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows key no registro determinam o comportamento da \_ infraestrutura AppInit DLLs. A tabela a seguir descreve esses valores de registro:



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

Todas as DLLs que são carregadas pela \_ infraestrutura AppInit DLLs devem ser assinadas por código. nos interesses da compatibilidade de aplicativos, o sistema operacional Windows 7 carregará todas as DLLs AppInit. no entanto, a Microsoft recomenda que todos os desenvolvedores de aplicativos codifiquem suas DLLs para ajudar a melhorar a confiabilidade de Windows e se preparar para a imposição de assinatura de código em versões futuras do Windows. a \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor em Windows 7 é definido como 0 por padrão.

**Windows Server 2008 R2**

Todas as DLLs que são carregadas pela \_ infraestrutura de DLLs AppInit devem ser assinadas por código. a \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor no Windows Server 2008 R2 é definido como 1 por padrão.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[AppInit DLLs no Windows 7 e Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
