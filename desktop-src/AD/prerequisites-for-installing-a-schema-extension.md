---
title: Pré-requisitos para instalar uma extensão de esquema
description: Para modificar o esquema, verifique se você tem os direitos a seguir e se está ciente das informações a seguir que você deve ter direitos suficientes para modificar o esquema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104293805"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Pré-requisitos para instalar uma extensão de esquema

Para modificar o esquema, verifique se você tem os direitos a seguir e se está ciente das seguintes informações:

-   Você deve ter direitos suficientes para modificar o esquema. O esquema contém todas as definições de dados para Active Directory Domain Services para toda a empresa. Para atualizar o esquema, um usuário deve ser membro do grupo Administradores de esquema ou ter recebido os direitos para atualizar o esquema.
-   Você só pode fazer alterações de esquema no mestre de esquema. Para obter mais informações, consulte [detectando o mestre de esquema](detecting-the-schema-master.md).
-   O mestre de esquema deve ser gravável; ou seja, o bloqueio de segurança no registro deve ser removido. Para obter mais informações, consulte [habilitando alterações de esquema no mestre de esquema](enabling-schema-changes-at-the-schema-master.md).
-   Para obter mais informações sobre como verificar se o mestre de esquema pode ser modificado e como alterar suas configurações, consulte "XADM: não é possível atualizar o esquema no proprietário do esquema" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




