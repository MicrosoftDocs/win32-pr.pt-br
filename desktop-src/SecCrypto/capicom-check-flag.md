---
description: Define as condições para as quais uma cadeia de certificados deve ser verificada.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: Enumeração de CAPICOM_CHECK_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CHECK_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 47b6168fb87ebbb65b07eadfe9adaf488934e252
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770352"
---
# <a name="capicom_check_flag-enumeration"></a>Enumeração de sinalizador de \_ verificação CApicom \_

O tipo de enumeração **\_ \_ sinalizador de verificação capicor** define as condições para as quais uma cadeia de certificados deve ser verificada.

## <a name="members"></a>Membros



| Membro                                          | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valor      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **verificação de CAPICOM \_ \_ None**                        | Nenhuma verificação de validade é feita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ verificar \_ \_ raiz confiável**               | Verifica se há uma raiz confiável da cadeia de certificados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **\_validade do \_ tempo de verificação de CAPICOM \_**              | Verifica a validade do tempo de todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **\_validade da \_ assinatura \_ verificar CAPICOM**         | Verifica se há assinaturas válidas em todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ verificar \_ \_ status de revogação online \_**  | Verifica o status de revogação de todos os certificados na cadeia usando listas de certificados revogados (CRLs) disponíveis online. As CRLs são baixadas usando a extensão de CDP (ponto de distribuição de CRL) no certificado. <br/> Se a CRL tiver sido baixada e não tiver expirado, capicor o usará e não ficará online. Se uma CRL não tiver sido baixada ou estiver desatualizada, capicor ficará online para tentar baixar a CRL.<br/> Esse sinalizador será ignorado se o capico de \_ verificação de \_ status de \_ revogação offline \_ também for especificado.<br/> | 0x00000008 |
| **CAPICOM \_ verificar \_ \_ status de revogação offline \_** | Verifica o status de revogação de todos os certificados na cadeia usando somente CRLs offline. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **\_ \_ cadeia completa de verificação de CAPICOM \_**             | Verifica a cadeia completa. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **\_restrições de \_ nome de verificação de CAPICOM \_**           | Verifica as restrições de nome. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **\_ \_ restrições básicas de verificação de CAPICOM \_**          | Verifica as restrições básicas. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **verificação de capicor \_ \_ período de validade aninhado \_ \_**    | Verifica a validade aninhada. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **capicot \_ verificar \_ \_ tudo online**                 | Verifica todas as condições, exceto capicor, \_ verificar \_ status de \_ revogação offline \_ . Verificações de revogação são executadas em todos os certificados na cadeia, exceto para o certificado raiz. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **capicore \_ verificar \_ offline \_ tudo**                | Verifica todas as condições, exceto capicor, \_ Verifique o \_ status de \_ revogação online \_ . Verificações de revogação são executadas em todos os certificados na cadeia, exceto para o certificado raiz. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




