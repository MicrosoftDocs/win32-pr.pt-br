---
title: Extensões de Binding-Handle RPC da Microsoft
description: As extensões da Microsoft para a linguagem IDL dão suporte a vários parâmetros de identificador que aparecem em posições diferentes do primeiro, o parâmetro mais à esquerda.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c93b68b20628bf6f7f65cee026412846e0b497d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475362"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Extensões de Binding-Handle RPC da Microsoft

As extensões da Microsoft para a linguagem IDL dão suporte a vários parâmetros de identificador que aparecem em posições diferentes do primeiro, o parâmetro mais à esquerda. As etapas a seguir descrevem a sequência que o compilador MIDL passa para resolver o parâmetro de identificador de associação no modo de compatibilidade DCE (/**uso**) e no modo padrão (Microsoft-Extended).

## <a name="dce-compatibility-mode"></a>Modo de compatibilidade do DCE

-   Identificador de associação que aparece na primeira posição.
-   Na extrema esquerda \[ , parâmetro [**de**](/windows/desktop/Midl/in) [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) \] .
-   Identificador de associação implícito especificado por \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] ou \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .
-   Se não houver um ACF presente, o padrão será o uso do \[ **\_ identificador auto** \] .

## <a name="default-mode"></a>Modo padrão

-   Identificador de ligação explícita mais à esquerda.
-   Identificador de associação implícito especificado por \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] ou \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .
-   Se não houver um ACF presente, o padrão será o uso do \[ [**\_ identificador auto**](/windows/desktop/Midl/auto-handle) \] .

Os compiladores de IDL do DCE procuram um identificador de associação explícito como o primeiro parâmetro. Quando o primeiro parâmetro não é um identificador de associação e um ou mais identificadores de contexto são especificados, o identificador de contexto mais à esquerda é usado como o identificador de associação. Quando o primeiro parâmetro não é um identificador e não há identificadores de contexto, o procedimento usa a associação implícita usando o \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) do atributo de ACF \] ou o \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .

As extensões da Microsoft para a IDL permitem que o identificador de ligação esteja em uma posição diferente do primeiro parâmetro. A extrema esquerda \[ [**no**](/windows/desktop/Midl/in) \] parâmetro de identificador explícito – se é um primitivo, definido pelo programador ou um identificador de contexto – é o identificador de associação. Quando não há parâmetros de identificador, o procedimento usa associação implícita usando o \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) do atributo ACF \] ou o \[ [**\_ identificador auto**](/windows/desktop/Midl/auto-handle) \] .

As regras a seguir se aplicam ao modo de compatibilidade do DCE (/OSF) e ao modo padrão:

-   A associação de identificador automático é usada quando nenhum ACF está presente.
-   \[ [](/windows/desktop/Midl/in) \] Os identificadores explícitos in ou \[ **in**, [**out**](/windows/desktop/Midl/out-idl) \] para uma função individual imprimem qualquer associação implícita especificada para a interface.
-   \[ [](/windows/desktop/Midl/in) \] \[  \] Não há suporte para vários identificadores primitivos in ou in.
-   Vários \[ [](/windows/desktop/Midl/in) \] \[ identificadores de contexto explícitos de entrada ou **de** saída \] são permitidos.
-   Todos os parâmetros de identificador definidos pelo programador, exceto o parâmetro Binding-Handle, são tratados como dados Transmissible.

A tabela a seguir contém exemplos e descreve como os identificadores de associação são atribuídos em cada modo de compilador.




| Exemplo | Descrição | 
|---------|-------------|
| <pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre> | Nenhum identificador explícito foi especificado. O identificador de associação implícito, especificado por [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] ou [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], é usado. Quando nenhum ACF estiver presente, um identificador automático será usado. | 
| <pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,           [in] short s );</code></pre> | Um identificador explícito do tipo handle_t é especificado. O parâmetro <em>H</em> é o identificador de associação para o procedimento. | 
| <pre class="syntax" data-space="preserve"><code>void proc3([in] short s,           [in] handle_t H );</code></pre> | O primeiro parâmetro não é um identificador. No modo padrão, o parâmetro de identificador mais à esquerda, <em>H</em>, é o identificador de associação. No modo/OSF, a associação implícita é usada. Um erro é relatado porque o segundo parâmetro deve ser transmissible e handle_t não pode ser transmitido. | 
| <pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;void proc1([in] short s,           [in] MY_HDL H );</code></pre> | O primeiro parâmetro não é um identificador. No modo padrão, o parâmetro de identificador mais à esquerda, <em>H</em>, é o identificador de associação. Os stubs chamam as rotinas fornecidas pelo usuário MY_HDL_bind e MY_HDL_unbind. No modo/uso, a associação implícita é usada. O parâmetro identificador <em>H</em> definido pelo programador é tratado como dados Transmissible. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;void proc1([in] MY_HDL H,            [in] MY_HDL p );</code></pre> | O primeiro parâmetro é um identificador de associação. O parâmetro <em>H</em> é o parâmetro de identificador de associação. O segundo parâmetro de identificador definido pelo programador é tratado como dados de Transmissible. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [context_handle] void * CTXT_HDL;void proc1([in] short s,           [in] long l,           [in] CTXT_HDL H ,           [in] char c);</code></pre> | O identificador de associação é um identificador de contexto. O parâmetro <em>H</em> é o identificador de associação. | 




 

 

 
