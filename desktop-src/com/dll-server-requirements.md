---
title: Requisitos do servidor DLL
description: Embora a maioria das DLLs possa ser executada em um substituto, algumas DLLs não podem.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 624b516f4b6c9deb00e3a093bd3531d3453e631450a1e5ec3b0810569580961a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993236"
---
# <a name="dll-server-requirements"></a>Requisitos do servidor DLL

Embora a maioria das DLLs possa ser executada em um substituto, algumas DLLs não podem.

O dll deve estar bem se comparado se você quiser usar o substituto fornecido pelo sistema. Por exemplo, uma DLL que chama métodos que registram retornos de chamada do cliente tentaria invocar esses retornos de chamada como se os ponteiros de função recebidos fossem instruções em seu espaço de endereço, o que não é o caso. Da mesma forma, uma DLL que usa uma variável global que espera que o cliente acesse não funcionaria. Em geral, os parâmetros que não podem ser corretamente empacotados impedirão que o servidor DLL seja executado fora do processo do cliente. Em muitos casos, você pode escrever um substituto personalizado especificamente projetado para compensar o comportamento "inadequado". (Para obter mais informações, consulte [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).)

Se o servidor DLL usar interfaces personalizadas, você precisará garantir que o código de marshaling esteja disponível para essas interfaces. Por exemplo, você pode criar e registrar uma DLL de proxy ou fornecer e registrar uma biblioteca de tipos que permitiria que o servidor funcionasse corretamente durante a execução em um substituto.

Os servidores DLL serão carregados somente em um processo substituto em execução no contexto de segurança adequado. O contexto de segurança para o substituto do servidor DLL é determinado da mesma maneira que para servidores EXE. O substituto do servidor DLL é executado no mesmo contexto de segurança que o cliente, a menos que um valor **runas** , que determina o contexto de segurança, seja definido na seção do registro [AppID](appid-clsid.md) do servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> </dl>

 

 




