---
title: Gadgets de área de trabalho removidos
description: Gadgets de área de trabalho removidos
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- miniaplicativo
- gadgets de área de trabalho
- Barra lateral do Windows
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104366802"
---
# <a name="desktop-gadgets-removed"></a>Gadgets de área de trabalho removidos

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows 8  
**Servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

Do ponto de vista da funcionalidade, os gadgets já foram preteridos e são descritos por novos blocos dinâmicos e aplicativos. Os gadgets também apresentam um risco de segurança aos usuários. Como plataforma, existem vulnerabilidades, de modo que até mesmo os gadgets benignos pudessem ser explorados. Portanto, para defender o Windows 8 como nosso sistema operacional mais moderno e seguro, optamos por remover os gadgets do sistema operacional inteiramente. Os usuários do Windows 7 com gadgets em sua área de trabalho serão notificados e os gadgets serão desinstalados.

## <a name="manifestation"></a>Manifestação

Os gadgets de área de trabalho não estarão disponíveis na área de trabalho do Windows.

## <a name="mitigation"></a>Atenuação

A estrutura de pastas e a API dos gadgets de área de trabalho permanecerão em vigor para o Windows 8. Os aplicativos que instalam e executam gadgets de forma programática usando essa API continuarão a ser executados sem falha (embora os próprios gadgets não sejam).

## <a name="solution"></a>Solução

Os desenvolvedores de aplicativos de área de trabalho não devem empacotar gadgets em seus instaladores. Esses gadgets ocuparão espaço para o usuário e não poderão ser executados no sistema.

## <a name="tests"></a>Testes

Os desenvolvedores podem testar a compatibilidade dessa alteração desabilitando o componente opcional para gadgets de área de trabalho no Windows 7. Para desabilitar gadgets em um PC com Windows 7, siga as etapas abaixo:

1.  Navegue para ativar ou desativar recursos do Windows no painel de controle.
2.  Desmarque a caixa ao lado de "plataforma de gadget do Windows".
3.  Clique em OK e siga as instruções adicionais na tela.

## <a name="resources"></a>Recursos

[Vulnerabilidades em gadgets podem permitir a execução remota de código](https://support.microsoft.com/kb/2719662)

 

 




