---
title: Reorganização
description: A organização de vendas foi movida para uma nova organização \ 8212; \ 0034; Vendas e suporte. \ 0034; Ela foi promovida a vice-presidente e conduzirá a nova organização.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- ADSI de reorganização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368b4db1909c50242e3eda1402e46896e54785aa66739b324995b7edbdd1b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690743"
---
# <a name="reorganization"></a>Reorganização

A organização de vendas foi movida para uma nova organização – "Vendas e suporte". Ela foi promovida a vice-presidente e conduzirá a nova organização. Joe Worden, o administrador corporativo, deve mover a UO de Vendas para uma nova UO, Vendas e Suporte.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Com este exemplo de código, todos os objetos na unidade organizacional de vendas, incluindo as unidades sub organizacionais, são movidos para a nova unidade organizacional.

Agora, Joe pode mover Julia para a unidade organizacional Vendas e Suporte.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Esteja ciente de que o link de relatório direto do gerente entre Julia Gray e Chris Gray é atualizado automaticamente pelo Active Directory.

**Para criar um relatório do Active Directory**

1.  Abra Visual Basic versão 6.0 e, quando solicitado para o tipo de projeto, selecione **Dados Project**.
2.  Em **Data Project**, clique duas vezes em Ambiente de **Dados1**.
3.  Na janela **Ambiente de Dados,** clique com o botão direito do mouse no objeto de **conexão (Connection1)** e selecione **Propriedades**.
4.  Selecione **OLE DB Provedor de Serviços de Diretório da Microsoft** e clique em **Próximo.**
5.  Selecione **Usar Windows NT Segurança integrada** e clique em **OK.** Isso cria um objeto de conexão.
6.  Clique com o botão direito do **mouse na janela Ambiente de** Dados novamente para selecionar Adicionar **Comando**. Clique com o botão direito **do mouse no objeto Command1** e selecione **Propriedades**. A caixa **de diálogo Propriedades do Command1** a seguir será exibida.

    ![caixa de diálogo propriedades command1](images/adadsi3.png)

7.  Clique no **botão SQL opção Instrução** e digite o seguinte:

    SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'

    O **objeto Command** é criado. Adicione o **objeto Command** ao relatório.

8.  Clique duas vezes **em Relatório de Dados1** na **Project** janela.
9.  Arraste o **objeto Command1** da **janela DataEnvironment1** para **a seção Detalhes** na janela **Relatório de** Dados.
10. Em **Propriedades de DataReport1**, para **DataSource**, selecione **DataEnvironment1** no menu suspenso e selecione **Command1** no campo **DataMember.**
11. Na janela do projeto, clique com o botão direito **do mouse em Data Project** e selecione Propriedades do **DataProject**.
12. Na janela **de diálogo DataProject - Project Propriedades,** em Objeto de Inicialização **,** selecione **DataReport1** no menu suspenso. Clique em **OK** para salvar.
13. Compilar. A caixa **de diálogo DataReport1 a** seguir será exibida.

    ![caixa de diálogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unindo dados heterogêneos](joining-heterogeneous-data.md)
</dt> </dl>

 

 




