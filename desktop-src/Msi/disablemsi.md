---
description: Se o valor dessa política de sistema por computador estiver definido como &\# 0034;2&0034; o instalador estará sempre desabilitado para todos os \# aplicativos. Se esse valor de política for definido como &\# 0034;1&0034;, o instalador será desabilitado para aplicativos não gerenciados, mas ainda será habilitado para aplicativos \# gerenciados.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846b8fb8c2c1127e59c82cce138a0956756d3447d6628cb61ef170a91e6290b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378554"
---
# <a name="disablemsi"></a>DisableMSI

Se o valor dessa política de sistema por [computador](system-policy.md) for definido como "2", o instalador estará sempre desabilitado para todos os aplicativos. Se esse valor de política for definido como "1", o instalador será desabilitado para aplicativos não gerenciados, mas ainda está habilitado para aplicativos gerenciados.

A tabela a seguir lista as possíveis configurações.



| DisableMSI | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Default*  | No Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se o valor da política for Nulo, ausente ou qualquer número diferente de 1 ou 2, o instalador do Windows será habilitado para aplicativos gerenciados. As instalação de aplicativos nãomanagedos são bloqueadas.<br/> No Windows XP, Windows Vista e Windows 7, o instalador Windows está habilitado para todos os aplicativos. Todas as operações de instalação são permitidas.<br/> |
| 0          | Windows O instalador está habilitado para todos os aplicativos. Todas as operações de instalação são permitidas.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | O Windows instalador está desabilitado para aplicativos não gerenciados, mas ainda está habilitado para aplicativos gerenciados. Instalações não elevadas por usuário são bloqueadas. As instalação por computador e elevadas por usuário são permitidas.                                                                                                                                                                                                                        |
| 2          | Windows O instalador sempre está desabilitado para todos os aplicativos. Nenhuma instalação é permitida, incluindo reparos, reinstalações ou instalações sob demanda.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




