---
title: Chave de Interface
description: Registra novas interfaces associando um nome de interface a uma ID de interface (IID). Deve haver uma subchave IID para cada nova interface.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chave do registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005877"
---
# <a name="interface-key"></a>Chave de Interface

Registra novas interfaces associando um nome de interface a uma ID de interface (IID). Deve haver uma subchave IID para cada nova interface.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_Interface de \\ \\ classes de \\ software de computador local** \\ *{* IID *}*



| Valor do Registro                               | Descrição                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifica a interface da qual a interface atual é derivada.                                  |
| [**NumMethods**](nummethods.md)             | Contém o número de métodos na interface associada, incluindo métodos de interfaces derivadas. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.                                                           |



 

## <a name="remarks"></a>Comentários

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface**](interface.md)
</dt> </dl>

 

 




