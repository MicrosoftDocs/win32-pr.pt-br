---
title: Reorganização
description: A organização de vendas mudou para uma nova organização \ 8212; \ 0034; Vendas e suporte. \ 0034; Julie Bankert foi promovido para Vice-Presidente e conduzirá a nova organização.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- ADSI de reorganização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004863"
---
# <a name="reorganization"></a>Reorganização

A organização de vendas mudou para uma nova organização: "vendas e suporte". Julie Bankert foi promovido para Vice-Presidente e conduzirá a nova organização. Joe Worden, administrador corporativo, deve mover a UO de vendas para uma nova UO, vendas e suporte.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Com este exemplo de código, todos os objetos na unidade organizacional Sales, incluindo as unidades de suborganização, são movidos para a nova unidade organizacional.

Agora, Joe pode mover Julie para a unidade organizacional Sales and Support.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Lembre-se de que o link de relatório direto de gerente entre Julie Bankert e Chris Gray é atualizado automaticamente pelo Active Directory.

**Para criar um relatório de Active Directory**

1.  Abra Visual Basic versão 6,0 e, quando solicitado, insira o tipo de projeto, selecione **projeto de dados**.
2.  Em **projeto de dados**, clique duas vezes em **Data Environment1**.
3.  Na janela **ambiente de dados** , clique com o botão direito do mouse no objeto de conexão **(Connection1)** e selecione **Propriedades**.
4.  Selecione **provedor de OLE DB para serviços de diretório da Microsoft** e clique em **Avançar**.
5.  Selecione **usar segurança integrada do Windows NT** e clique em **OK**. Isso cria um objeto de conexão.
6.  Clique com o botão direito do mouse na janela **ambiente de dados** novamente para selecionar **Adicionar comando**. Clique com o botão direito do mouse no objeto **Command1** e selecione **Propriedades**. A caixa de diálogo **Command1 Properties** a seguir será exibida.

    ![caixa de diálogo Propriedades do Command1](images/adadsi3.png)

7.  Clique no botão de opção **instrução SQL** e digite o seguinte:

    Selecione o nome, telephoneNumber de ' LDAP://DC = Fabrikam, DC = com ' em que objectCategory = ' Person ' e objectClass = ' user '

    O objeto de **comando** é criado. Adicione o objeto de **comando** ao relatório.

8.  Clique duas vezes em **Data Report1** na janela do **projeto** .
9.  Arraste o objeto **Command1** da janela **DataEnvironment1** para a seção **detalhes** na janela **relatório de dados** .
10. Em **Propriedades de DataReport1**, para **DataSource**, selecione **DataEnvironment1** no menu suspenso e selecione **Command1** no campo **DataMember** .
11. Na janela do projeto, clique com o botão direito do mouse em **projeto de dados** e selecione **Propriedades do dataproject**.
12. Na janela de diálogo **dataproject – Project Properties** , em **Startup object**, selecione **DataReport1** no menu suspenso. Clique em **OK** para salvar.
13. Compilar. A caixa de diálogo **DataReport1** a seguir será exibida.

    ![caixa de diálogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unindo dados heterogêneos](joining-heterogeneous-data.md)
</dt> </dl>

 

 




