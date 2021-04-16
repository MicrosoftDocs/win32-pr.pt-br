---
description: 'As constantes RENDBIND são sinalizadores usadas pelo método ITDirectory:: BIND para indicar os tipos de autenticação fornecidos.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes de RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779301"
---
# <a name="rendbind_-constants"></a>\_Constantes RENDBIND

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

As constantes RENDBIND são sinalizadores usadas pelo método [**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) para indicar os tipos de autenticação fornecidos.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND \_ autenticar**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Autenticar usuário.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTdomainname**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Use o nome de domínio padrão.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTusername**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Use o nome de usuário padrão.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTpassword**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Use a senha padrão.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTcredentials**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Os três vinculantes anteriores juntos para sua conveniência.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




