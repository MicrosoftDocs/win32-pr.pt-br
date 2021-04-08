---
description: O sistema carrega um provedor de tempo com base em suas informações de configuração armazenadas no registro.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrando um provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828683"
---
# <a name="registering-a-time-provider"></a>Registrando um provedor de tempo

O sistema carrega um provedor de tempo com base em suas informações de configuração armazenadas no registro. Cada provedor de tempo deve criar a seguinte chave do registro:

**HKEY \_ \_ \\ Sistema de máquina local** \\ **CurrentControlSet** \\ **Serviços** \\ **W32Time** \\ **timefornecedores** \\ *ProviderName*

A tabela a seguir descreve os valores que devem existir na chave de cada provedor.



| Valor             | Descrição                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | O nome da DLL que contém o provedor. Esse valor tem o tipo **reg \_ sz**.                                                                                                                                     |
| **Enabled**       | Indica se o provedor deve ser iniciado. Se esse valor for 1, o provedor será iniciado. Caso contrário, o provedor não será iniciado. Esse valor tem o tipo **reg \_ DWORD**.                                           |
| **InputProvider** | Indica se o provedor é um provedor de entrada ou um provedor de saída. Se esse valor for 1, o provedor será um provedor de entrada. Caso contrário, o provedor será um provedor de saída. Esse valor tem o tipo **reg \_ DWORD**. |



 

O Gerenciador de provedores de tempo enumera as chaves sob a chave **Timefornecedores** e inicia cada provedor habilitado. Os provedores são iniciados na inicialização do sistema e sempre que há alterações de parâmetro.

Cada provedor de tempo também pode armazenar informações de configuração específicas do aplicativo no registro.

 

 



