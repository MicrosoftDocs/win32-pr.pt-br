---
description: Os identificadores a seguir são usados para identificar uma interface criptográfica de CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificadores de interface CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ebadf561df916eedde1175a39911da55628b113022378cee9e74b61d021792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908266"
---
# <a name="cng-interface-identifiers"></a>Identificadores de interface CNG

Os identificadores a seguir são usados para identificar uma interface criptográfica de CNG. Na CNG, uma interface identifica o tipo de comportamento criptográfico que um provedor suporta. Por exemplo, um provedor pode ser um gerador de números aleatórios ou pode ser um provedor de hash.



| Constante/valor                                                                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ \_Interface de codificação**</dt> <dt>0x00000001</dt> </dl>                                               | A interface de codificação simétrica.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ \_Interface de hash**</dt> <dt>0x00000002</dt> </dl>                                                     | A interface de hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interface de criptografia assimétrica**</dt> <dt>0x00000003</dt> </dl> | A interface de criptografia assimétrica.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interface de contrato de segredo**</dt> <dt>0x00000004</dt> </dl>                | A interface do contrato secreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ \_Interface de assinatura**</dt> <dt>0x00000005</dt> </dl>                                      | A interface da assinatura.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ RNG \_ interface**</dt> <dt>0x00000006</dt> </dl>                                                        | A interface do gerador de números aleatórios.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interface de armazenamento de chave**</dt> <dt>0x00010001</dt> </dl>                               | A interface de armazenamento de chaves.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ \_Interface Schannel**</dt> <dt>0x00010002</dt> </dl>                                         | A interface de assinatura Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interface de assinatura Schannel**</dt> <dt>0x00010003</dt> </dl>          | A interface do pacote de codificação Schannel.<br/> **Windows server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000:** Não há suporte para esse valor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Bcrypt. h; </dt> <dt>NCrypt. h</dt> </dl> |



 

 




