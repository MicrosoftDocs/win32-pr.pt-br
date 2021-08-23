---
title: Chave de Interface
description: Registra novas interfaces associando um nome de interface a uma ID de interface (IID). Deve haver uma sub-chave IID para cada nova interface.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chave do Registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda0cc29331521025a9274dca7b85080be2ddd5a9b631d2660eadaa13fe4941a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048144"
---
# <a name="interface-key"></a>Chave de Interface

Registra novas interfaces associando um nome de interface a uma ID de interface (IID). Deve haver uma sub-chave IID para cada nova interface.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_Interface CLASSES DE SOFTWARE \\ \\ DE \\** COMPUTADOR LOCAL \\ *{* IID *}*



| Valor do Registro                               | Descrição                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Baseinterface**](baseinterface.md)       | Identifica a interface da qual a interface atual é derivada.                                  |
| [**NumMethods**](nummethods.md)             | Contém o número de métodos na interface associada, incluindo métodos de interfaces derivadas. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Mapas um IID para um CLSID em DLLs de proxy de 16 bits.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Mapas um IID para um CLSID em DLLs de proxy de 32 bits.                                                           |



 

## <a name="remarks"></a>Comentários

A **chave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde à chave **\_ \_ RAIZ de CLASSES HKEY,** que foi mantida para compatibilidade com versões anteriores do COM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface**](interface.md)
</dt> </dl>

 

 




