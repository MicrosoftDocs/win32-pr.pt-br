---
description: A interface IX509EndorsementKey expõe os métodos a seguir.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Métodos IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171820"
---
# <a name="ix509endorsementkey-methods"></a>Métodos IX509EndorsementKey

A interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expõe os métodos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                        | Descrição                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método addcertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Adicione um certificado de chave de endosso ao KSP (provedor de armazenamento de chaves) que oferece suporte a chaves de endosso.<br/>                                                                                                                                                                                     |
| [**Método Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Fecha a chave de endosso. Você só pode chamar o método [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) depois que o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) tiver sido chamado com êxito.<br/>                                                                                              |
| [**Método ExportPublicKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Exporta a chave pública de endosso.<br/>                                                                                                                                                                                                                                                      |
| [**Método GetCertificateByIndex**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Obtém o certificado de endosso associado à chave de endosso do provedor de armazenamento de chaves para o índice especificado.<br/>                                                                                                                                                              |
| [**Método GetCertificateCount**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Obtém a contagem dos certificados de endosso no provedor de armazenamento de chaves.<br/>                                                                                                                                                                                                              |
| [**Método Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Abre a chave de endosso. A chave de endosso deve ser aberta antes que você possa recuperar uma informação da chave de endosso, adicionar ou remover certificados ou exportar a chave de endosso.<br/>                                                                                                  |
| [**Método RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Remove um certificado de endosso relacionado à chave de endosso do provedor de armazenamento de chaves. Você só pode chamar o método [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) depois que o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) tiver sido chamado com êxito.<br/> |



 

 

 




