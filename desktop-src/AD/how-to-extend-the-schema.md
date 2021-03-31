---
title: Como estender o esquema
description: Quando as classes e/ou atributos existentes não se ajustarem ao tipo de dados que você deseja armazenar, talvez você queira estender o esquema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- AD Schema, como estender
- Active Directory, usando, esquema
- Active Directory, usando, esquema, estendendo o esquema, como estender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640398"
---
# <a name="how-to-extend-the-schema"></a>Como estender o esquema

Quando as classes e/ou atributos existentes não se ajustarem ao tipo de dados que você deseja armazenar, talvez você queira estender o esquema. Para obter mais informações sobre como decidir quando estender o esquema, consulte [estendendo o esquema](extending-the-schema.md). Quando você tiver decidido que a extensão do esquema é necessária, use o procedimento a seguir para estender o esquema.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Verifique Active Directory funcionalidade antes de aplicar as extensões de esquema

Verifique Active Directory funcionalidade antes de atualizar o esquema para ajudar a garantir que a extensão do esquema continue sem erros. No mínimo, verifique se todos os controladores de domínio da floresta estão online e executando a replicação de entrada.

**Para verificar Active Directory funcionalidade antes de aplicar a extensão do esquema**

1.  Faça logon em uma estação de trabalho administrativa que tenha a ferramenta de suporte do Windows Repadmin.exe instalada.
    > [!Note]  
    > As ferramentas de suporte estão localizadas na mídia de instalação do sistema operacional na \\ pasta ferramentas de suporte.

     

2.  Abra um prompt de comando e, em seguida, altere os diretórios para a pasta na qual as ferramentas de suporte do Windows estão instaladas.
3.  Em um prompt de comando, digite o seguinte e pressione ENTER:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Todos os controladores de domínio devem mostrar 0 na coluna falha e os maiores deltas (que indicam o número de alterações feitas no banco de dados de Active Directory desde a última replicação bem-sucedida) devem ser menores ou aproximadamente iguais à frequência de replicação do link de site usado pelo controlador de domínio para replicação. A frequência de replicação padrão é 180 minutos.

    Para obter mais informações sobre as etapas adicionais que você pode executar para verificar Active Directory funcionalidade antes de aplicar a extensão do esquema, consulte o [artigo 325379 na base de dados de conhecimento Microsoft](https://support.microsoft.com/kb/325379/en-us).

**Para estender o esquema**

1.  Determine o método de extensão. Depois de criar cuidadosamente as alterações de esquema, a próxima etapa é decidir qual método usar para estender o esquema. É possível usar um dos seguintes métodos:
    -   Manualmente, usando arquivos de importação. Consulte a documentação [usando a ferramenta Ldifde](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > Não use o LDIFDE para importar \* arquivos. ldf do Windows SCH. Esses arquivos são necessários para estender o esquema de Active Directory a fim de instalar controladores de domínio que executam uma versão mais recente do Windows Server do que a versão em execução no mestre de esquema atual. Quando você precisar estender o esquema para instalar um novo controlador de domínio, use Adprep.exe.

         

    -   Programaticamente, usando um programa de instalação. Para obter mais informações, consulte [extensão programática](programmatic-extension.md)
2.  Habilitar alterações de esquema. Para obter mais informações, consulte [pré-requisitos para instalar uma extensão de esquema](prerequisites-for-installing-a-schema-extension.md) e [habilitar alterações de esquema no mestre de esquema](enabling-schema-changes-at-the-schema-master.md).
3.  Obtenha um OID (identificador de objeto) para seus novos atributos e/ou classes, conforme descrito em [obtendo um identificador de objeto](obtaining-an-object-identifier.md).
4.  Crie novos atributos e classes.
5.  Use especificadores de exibição para integrar novos atributos e classes com a interface do usuário, se necessário.
6.  Atualize o cache de esquema conforme descrito em [atualizando o cache de esquema](updating-the-schema-cache.md).
7.  Verifique a extensão do esquema usando LDP.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo um identificador de objeto](obtaining-an-object-identifier.md)
</dt> <dt>

[As novas ferramentas de linha de comando para Active Directory no Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Usando a ferramenta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Estendendo o esquema de Active Directory](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restrições na extensão do esquema](restrictions-on-schema-extension.md)
</dt> </dl>

 

 