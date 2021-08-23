---
title: Gadgets de área de trabalho removidos
description: Gadgets de área de trabalho removidos
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- miniaplicativo
- gadgets de área de trabalho
- Windows Forma
- Forma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707006"
---
# <a name="desktop-gadgets-removed"></a>Gadgets de área de trabalho removidos

## <a name="platforms"></a>Plataformas

 **clientes** -Windows 8  
**servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

Do ponto de vista da funcionalidade, os gadgets já foram preteridos e são descritos por novos blocos dinâmicos e aplicativos. Os gadgets também apresentam um risco de segurança aos usuários. Como plataforma, existem vulnerabilidades, de modo que até mesmo os gadgets benignos pudessem ser explorados. portanto, para defender Windows 8 como nosso sistema operacional mais moderno e seguro, optamos por remover os gadgets do sistema operacional inteiramente. os usuários do Windows 7 com gadgets em sua área de trabalho serão notificados e os gadgets serão desinstalados.

## <a name="manifestation"></a>Manifestação

os gadgets de área de trabalho não estarão disponíveis na área de trabalho Windows.

## <a name="mitigation"></a>Atenuação

A estrutura de pastas e a API dos gadgets de área de trabalho permanecerão em vigor para Windows 8. Os aplicativos que instalam e executam gadgets de forma programática usando essa API continuarão a ser executados sem falha (embora os próprios gadgets não sejam).

## <a name="solution"></a>Solução

Os desenvolvedores de aplicativos de área de trabalho não devem empacotar gadgets em seus instaladores. Esses gadgets ocuparão espaço para o usuário e não poderão ser executados no sistema.

## <a name="tests"></a>Testes

os desenvolvedores podem testar a compatibilidade dessa alteração desabilitando o componente opcional para gadgets de área de trabalho no Windows 7. para desabilitar gadgets em um computador Windows 7, siga as etapas abaixo:

1.  navegue para ativar ou desativar recursos do Windows no painel de controle.
2.  desmarque a caixa ao lado de "Windows a plataforma de Gadget".
3.  Clique em OK e siga as instruções adicionais na tela.

## <a name="resources"></a>Recursos

[Vulnerabilidades em gadgets podem permitir a execução remota de código](https://support.microsoft.com/kb/2719662)

 

 




