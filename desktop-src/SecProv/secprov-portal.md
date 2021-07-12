---
description: Os provedores WMI de segurança podem ser usados para scripts WMI e para criar um provedor de segurança gerenciado.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Provedores WMI de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581984"
---
# <a name="security-wmi-providers"></a>Provedores WMI de segurança

## <a name="purpose"></a>Finalidade

os provedores de segurança WMI permitem que administradores e programadores configurem Criptografia de Unidade de Disco BitLocker (BDE) e o Trusted Platform Module (TPM) usando Instrumentação de Gerenciamento do Windows (WMI).

## <a name="developer-audience"></a>Público de desenvolvedores

este documento especifica a interface do provedor WMI para gerenciar e configurar Criptografia de Unidade de Disco BitLocker (BDE) e Trusted Platform Module (TPM) no Windows server 2008 R2 e Windows Server 2008 para servidores e Windows 7 e Windows Vista para computadores cliente. Ele se destina a ser lido por esses scripts de escrita, elementos de interface do usuário ou outras ferramentas administrativas para o BDE ou o TPM.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Os provedores de WMI de segurança exigem o arquivo. mof especificado com cada provedor e um sistema operacional com suporte. o sistema operacional mínimo é o Windows Server 2008 ou o Windows Vista. Criptografia de Unidade de Disco BitLocker só está disponível para as versões do Windows vista Enterprise e Windows vista Ultimate do Windows vista. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                               | Descrição                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Sobre provedores WMI de segurança](about-security-wmi-providers.md)<br/>         | Breve visão geral dos provedores de WMI de segurança.<br/>           |
| [Referência de provedores WMI de segurança](security-wmi-providers-reference.md)<br/> | Documentação de referência para os provedores de WMI de segurança.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionais

A seguir estão os recursos adicionais.



| Recurso     | Descrição                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classes      | Para obter mais informações sobre os provedores de WMI de segurança, consulte [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ TPM**](win32-tpm.md). |



 

 

 




