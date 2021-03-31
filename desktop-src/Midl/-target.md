---
title: opção /target
description: A opção/target permite que o compilador MIDL habilite otimizações disponíveis somente em versões recentes do Windows. A opção/target ativa automaticamente opções adicionais.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /Target switch MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104011892"
---
# <a name="target-switch"></a>opção /target

A opção **/target** permite que o compilador MIDL habilite otimizações disponíveis somente em versões recentes do Windows. A opção **/target** ativa automaticamente opções adicionais.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*level* 
</dt> <dd>

Especifica o nível de destino, como NT50, NT51, NT60, NT61, NT62 ou NT100.

</dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/target** ativa automaticamente opções adicionais, com base no sistema operacional, conforme especificado na tabela a seguir:



| Sistema operacional | nível de/Target | Opções ativadas                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/Error All/robust               |
| Windows XP       | NT51          | /Oicf/Error All/robust/Protocol |
| Windows Vista    | NT60          | /Oicf/Error All/robust/Protocol |
| Windows 7        | NT61          | /Oicf/Error All/robust/Protocol |
| Windows 8        | NT62          | /Oicf/Error All/robust/Protocol |
| Windows 10       | NT100         | /Oicf/Error All/robust/Protocol |
 

Para garantir que um stub seja executado no sistema especificado pela opção **/target** , o MIDL emite um erro quando um recurso disponível somente em uma versão mais recente do Windows estiver presente. A tabela a seguir especifica o nível de **/target** mínimo necessário para habilitar o recurso. Níveis de destino mais altos incluem todos os recursos de níveis de destino inferiores.



| Nível de/Target necessário mínimo | Recursos                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /robust<br/> \[message\]<br/> \[async\]<br/> \[\_UUID assíncrono\]<br/> \[notificar \] no modo/Oicf<br/> \[codificar \] ou \[ decodificar \] no modo/Oicf<br/>                   |
| NT51                           | suporte a/Protocol de 64 bits<br/> \[\_ignorar parcial\]<br/> \[forçar \_ alocação\]<br/>                                                                                                 |
| NT60                           | Marshalling de estrutura complexa forçada<br/> Identificadores de contexto em uma matriz ou estrutura<br/> \[\]suporte de intervalo para cadeias de caracteres sem tamanho<br/> \[tipo \_ de \_ identificador de contexto estrito \_\]<br/> |
| NT61                           | As chamadas diretas de stub de COM para interfaces com menos de 32 métodos exigem a vinculação de stubs com com **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Suporte a ARM<br/> Suporte do WinRT<br/>                                                                                                                                                   |
| NT100                          | \[suporte a system_handle \]<br /> |


 

## <a name="examples"></a>Exemplos

**MIDL/Target NT50**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
