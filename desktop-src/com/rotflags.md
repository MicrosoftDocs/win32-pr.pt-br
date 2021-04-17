---
title: ROTFlags
description: Controla o registro de um servidor COM na corrompidos (tabela de objetos em execução).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- COM valor do registro ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813712"
---
# <a name="rotflags"></a>ROTFlags

Controla o registro de um servidor COM na corrompidos (tabela de objetos em execução).

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor de sinalizador | Constante                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>Descrição do ROTREGFLAGS \_ ALLOWANYCLIENT

Se um servidor COM quiser se registrar no corrompidos e permitir que qualquer cliente acesse o registro, ele deverá usar o sinalizador **ROTFLAGS \_ ALLOWANYCLIENT** . Um servidor COM "Activate as Activator" não pode especificar **ROTFLAGS \_ ALLOWANYCLIENT** porque o DCOMSCM (Gerenciador de controle de serviço) do DCOM impõe uma verificação de falsificação nesse sinalizador. Portanto, no Windows Vista e posterior, o COM adiciona suporte para a entrada de registro **ROTFlags** que permite ao servidor estipular que seus registros corrompidos são disponibilizados para qualquer cliente.

A entrada deve existir no hive **do \_ \_ computador local hKey** . Essa entrada fornece um servidor "Activate as Activator" com a mesma funcionalidade que o **ROTFLAGS \_ ALLOWANYCLIENT** fornece para um servidor runas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chave AppID](appid-key.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




