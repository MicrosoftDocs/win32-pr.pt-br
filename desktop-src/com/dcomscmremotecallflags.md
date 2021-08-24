---
title: DCOMSCMRemoteCallFlags
description: Controla o comportamento de chamadas do Gerenciador de controle de serviço (DCOMSCM) local DCOM para um DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- COM valor do registro DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d658b80d347e684aa42aebad936a863b9bca2138b3118508849a730e11878d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678825"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controla o comportamento de chamadas do Gerenciador de controle de serviço (DCOMSCM) local DCOM para um DCOMSCM remoto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor | Descrição                                       |
|-------|---------------------------------------------------|
| 0x1   | **a \_ ativação do DCOMSCM \_ usa \_ todos os \_ AUTHNSERVICES**  |
| 0x2   | **\_ativação DCOMSCM \_ \_ não permitir chamada não segura \_** |
| 0x4   | **DCOMSCM \_ resolver \_ usar \_ todos os \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ resolver \_ \_ não permitir chamada não segura \_**    |
| 0x10  | **DCOMSCM \_ ping \_ use \_ mid \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ ativação \_ use \_ todas as \_ AUTHNSERVICES descrição

Quando o cliente emite uma solicitação de ativação que usa as configurações de segurança padrão, o DCOMSCM local usa o serviço de autenticação Negotiate ao fazer a chamada RPC de ativação para o DCOMSCM remoto. Se a chamada falhar, o DCOMSCM local fará a chamada RPC de ativação usando sem segurança.

**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de ativação que usa o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de ativação usando Kerberos, NTLM ou outros provedores de segurança configurados. Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de ativação usando sem segurança.

ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista. Não é recomendável definir esse sinalizador, a menos que necessário por motivos de compatibilidade.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>\_Descrição da \_ \_ chamada não segura de DCOMSCM Activation inallow \_

Se o sinalizador de **\_ \_ \_ \_ chamada não segura de ativação DCOMSCM** for definido, o DCOMSCM local não fará uma chamada RPC de ativação não segura. Para permitir que os clientes façam solicitações de ativação com configurações de segurança não padrão, especifique a estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) ao fazer a solicitação de ativação. Nesse caso, a **ativação do \_ DCOMSCM \_ usa \_ todas as \_ AUTHNSERVICES** e a **ativação do DCOMSCM não permitir sinalizadores de \_ \_ \_ \_ chamada não seguros** são ignorados.

Não é recomendável definir esse sinalizador, a menos que todos os clientes e servidores na rede estejam totalmente autenticados.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ resolver \_ usar \_ todas as \_ AUTHNSERVICES descrição

Quando o cliente desempacotar uma referência de objeto, o DCOMSCM local usará o serviço de autenticação Negotiate ao fazer a chamada RPC de resolução OXID para o DCOMSCM remoto. Se a chamada falhar, o DCOMSCM local fará a chamada RPC de resolução OXID usando sem segurança.

**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de resolução OXID usando o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de resolução OXID usando Kerberos, NTLM ou outros provedores de segurança configurados. Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de resolução OXID usando sem segurança.

ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista. Não é recomendável definir esse sinalizador, a menos que necessário por motivos de compatibilidade.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ resolver \_ \_ não permitir descrição da chamada não segura \_

Se o sinalizador de **chamada não segura de DCOMSCM \_ resolver não \_ \_ seguro \_** estiver definido, o DCOMSCM local não fará uma chamada RPC de resolução oxid não segura. Além disso, o DCOMSCM local não faz uma chamada RPC de ping de coleta de lixo sem segurança. Não é recomendável definir esse sinalizador, a menos que todos os clientes e servidores na rede estejam totalmente autenticados.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ ping \_ use \_ média \_ AUTHNSERVICE descrição

O DCOMSCM local usa o serviço de autenticação Negotiate ao fazer a chamada RPC de ping de coleta de lixo para o DCOMSCM remoto. Se a chamada falhar, o local DCOMSCM fará a chamada RPC de ping de coleta de lixo usando sem segurança.

**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de ping de coleta de lixo usando o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de ping de coleta de lixo usando Kerberos, NTLM e outros provedores de segurança configurados. Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de ping de coleta de lixo usando sem segurança.

ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista. Não é recomendável definir o sinalizador **DCOMSCM \_ de \_ uso \_ de \_ AUTHNSERVICE médio** , a menos que necessário por motivos de compatibilidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação para conexões remotas](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 