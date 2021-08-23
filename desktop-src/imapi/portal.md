---
title: API de mestre de imagem
description: API de mestre de imagem
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28f98422a1845234ec9eda7054978797c876a41a905484a95a505bdf4e133c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611786"
---
# <a name="image-mastering-api"></a>API de mestre de imagem

## <a name="purpose"></a>Finalidade

a API de mestre de imagem do Microsoft Windows permite que os aplicativos testem e gravem imagens em mídia de armazenamento óptico de CD, DVD e Blu-ray. Outra mídia semelhante a um disco que deite imagens da mesma maneira também pode usar essa API.

## <a name="developer-audience"></a>Público de desenvolvedores

o imapi foi criado para desenvolvedores de C/C++ e Visual Basic e aqueles que escrevem scripts usando o VBScript.

O conhecimento de tecnologias de CD, DVD e Blu-Ray e sistemas de arquivos é recomendado. Os desenvolvedores podem se beneficiar de uma familiaridade com a revisão mais recente do comando de multimídia (MMC) em [ftp://ftp.T10.org/T10/Drafts/MMC6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

há suporte nativo para o imapi 2,0 a partir do Windows Vista e do Windows Server 2008. a habilitação da funcionalidade imapi 2,0 para Windows XP e Windows Server 2003 requer a instalação do pacote de atualização do [KB932716](https://support.microsoft.com/kb/932716) . se esse pacote não estiver instalado, o Windows XP ainda oferecerá suporte nativo ao [imapi 1,0](imapiv1.md).

> [!Note]  
> o Feature Pack Windows para Armazenamento está disponível para o público por meio do [centro de Download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05). Informações adicionais sobre alterações de API específicas podem ser encontradas na seção [o que há de novo](what-s-new.md) .

 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                             | Descrição                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novidades](what-s-new.md)<br/>           | Informações detalhando cada versão significativa da API de mestre de imagem.<br/> |
| [Sobre o IMAPi](about-imapi.md)<br/>         | Informações gerais sobre a API de mestre de imagem.<br/>                         |
| [Usando o IMAPi](using-imapi.md)<br/>         | Tópicos relacionados a tarefas que demonstram como usar a API de mestre de imagem.<br/>   |
| [Referência de IMAPi](imapi-reference.md)<br/> | Descrições detalhadas de interfaces IMAPi e outros elementos de programação.<br/>  |



 

## <a name="additional-resources"></a>Recursos adicionais

Mais informações sobre o IMAPi e outros assuntos relacionados podem ser encontradas nos seguintes locais:



| Tópico                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog de Armazenamento óptico da Microsoft](/archive/blogs/opticalstorage/)                | Realça os tópicos que se concentram na implementação da API de mestre de imagem em cenários de desenvolvimento do mundo real.                                                                                                                                                                                                                                                 |
| [Fórum de discussão sobre plataforma ótica](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Discuta CDROM.SYS, IMAPIv2 e problemas do sistema de arquivos dinâmicos. Este fórum se concentra em tópicos de nível de sistema e destina-se a desenvolvedores de aplicativos em vez de endusers.                                                                                                                                                                                                 |
| [Comitê Técnico T10](https://www.t10.org/)                       | Um comitê técnico do Comitê Internacional de padrões de tecnologia da informação (INCITS, pronunciado "insights"). O INCITS é reconhecido pelo e opera em regras que são aprovadas pelo American National Standards Institute (ANSI). Essas regras foram projetadas para garantir que os padrões voluntários sejam desenvolvidos pelo consenso de grupos do setor. |
| [OSTA (associação de tecnologia de Armazenamento óptica)](http://www.osta.org/) | trabalha para moldar o futuro do setor por meio de reuniões regulares de COSA (aplicativos ópticos de Armazenamento comercial), compatibilidade com DVD, Marketing, MPV (MusicPhotoVideo), comitês UDF e um novo comitê de Laser azul adhoc. Empresas interessadas em todo o mundo são convidadas para participar da organização e participar de seus comitês e programas.               |



 

 

