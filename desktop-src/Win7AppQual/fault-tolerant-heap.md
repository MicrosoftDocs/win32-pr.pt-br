---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap tolerante a falhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813356"
---
# <a name="fault-tolerant-heap"></a>Heap tolerante a falhas

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes-** Windows 7  

## <a name="feature-impact"></a>Impacto do recurso

 **Severidade-** Médio  
**Frequência-** Pequena  


## <a name="description"></a>Descrição

O FTH (heap tolerante a falhas) é um subsistema do Windows 7 responsável por monitorar falhas do aplicativo e aplicar mitigações de forma autônoma para evitar falhas futuras por aplicativo. Para a grande maioria dos usuários, o FTH funcionará sem a necessidade de intervenção ou alteração em sua parte. No entanto, em alguns casos, os desenvolvedores de aplicativos e os testadores de software podem precisar substituir o comportamento padrão desse sistema.

## <a name="solution"></a>Solução

**Exibindo a atividade de heap tolerante a falhas**

O heap tolerante a falhas registra informações quando o serviço é iniciado, interrompe ou começa a atenuar problemas de um novo aplicativo. Para exibir essas informações, siga estas etapas:

1.  Clique no menu Iniciar.
2.  Clique com o botão direito do mouse em **computador** e clique em **gerenciar**.
3.  Clique em **Visualizador de eventos**  >  **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows > tolerância a falhas-heap**
4.  Exibir eventos de FTH.

Os eventos stop e Start do serviço não contêm dados adicionais. O evento habilitado para FTH contém a ID do processo (PID), o nome da imagem do processo e a hora de início da instância do processo.

**Desabilitando o heap tolerante a falhas**

**Cuidado** Problemas sérios podem ocorrer se você modificar o registro incorretamente usando o editor do registro ou usando outro método. Esses problemas podem exigir a reinstalação do sistema operacional. A Microsoft não garante que esses problemas possam ser solucionados. Modifique o Registro por conta própria.  
 Para desabilitar completamente o heap tolerante a falhas em um sistema, defina o valor do REG \_ DWORD como **HKLM \\ software \\ Microsoft \\ FTH \\ habilitado** como **0**.

Depois de alterar esse valor, reinicie o sistema. O FTH não será mais ativado para novos aplicativos.

**Redefinindo a lista de aplicativos rastreados pelo FTH**

O heap tolerante a falhas é autogerenciável e interromperá a aplicação de forma autônoma, caso as atenuações não sejam efetivas para um determinado aplicativo. No entanto, se você precisar redefinir a lista de aplicativos para os quais o FTH está atenuando problemas (por exemplo, se você estiver testando um aplicativo e precisar reproduzir uma falha que o FTH está mitigando), poderá executar o seguinte comando em um prompt de comando elevado:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**  
**Cuidado** A execução desse comando limpará todos os aplicativos FTH, para que os aplicativos que estão funcionando corretamente no momento possam começar a falhar novamente após a execução desse comando.  

 

 



