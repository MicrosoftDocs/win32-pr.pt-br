---
description: Define as condições para as quais uma cadeia de certificados deve ser verificada.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: CAPICOM_CHECK_FLAG enumeração (Capicom.h)
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
ms.openlocfilehash: 4b9fbc5ec1717acbd32c70ea3467465daf47de5d41af794a5164f44174a602d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772508"
---
# <a name="capicom_check_flag-enumeration"></a>Enumeração CAPICOM \_ CHECK \_ FLAG

O **tipo de enumeração \_ CAPICOM CHECK \_ FLAG** define as condições para as quais uma cadeia de certificados deve ser verificada.

## <a name="members"></a>Membros



| Membro                                          | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valor      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ CHECK \_ NONE**                        | Nenhuma verificação de validade é feita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**               | Verifica se há uma raiz confiável da cadeia de certificados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **VALIDADE DO TEMPO \_ \_ DE VERIFICAÇÃO DO CAPICOM \_**              | Verifica a validade de tempo de todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **VALIDADE DA ASSINATURA DE VERIFICAÇÃO CAPICOM \_ \_ \_**         | Verifica se há assinaturas válidas em todos os certificados na cadeia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ VERIFICAR O STATUS DE \_ \_ REVOGAÇÃO \_ ONLINE**  | Verifica o status de revogação de todos os certificados na cadeia usando CRLs (listas de certificados revogados) disponíveis online. As CRLs são baixadas usando a extensão CDP (ponto de distribuição de CRL) no certificado. <br/> Se a CRL tiver sido baixada e não tiver expirado, o CAPICOM a usará e não será online. Se uma CRL não tiver sido baixada ou estiver desacompactada, o CAPICOM fica online para tentar baixar a CRL.<br/> Esse sinalizador será ignorado se CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS também for especificado.<br/> | 0x00000008 |
| **CAPICOM \_ VERIFICAR O STATUS DE \_ \_ REVOGAÇÃO \_ OFFLINE** | Verifica o status de revogação de todos os certificados na cadeia usando apenas CRLs offline. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **CADEIA COMPLETA DE VERIFICAÇÃO CAPICOM \_ \_ \_**             | Verifica a cadeia completa. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **RESTRIÇÕES DE NOME DE VERIFICAÇÃO CAPICOM \_ \_ \_**           | Verifica restrições de nome. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **CAPICOM \_ VERIFICAR \_ \_ RESTRIÇÕES BÁSICAS**          | Verifica as restrições básicas. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **PERÍODO DE VALIDADE \_ \_ ANINHADO DE \_ VERIFICAÇÃO DO CAPICOM \_**    | Verifica a validade aninhada. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ CHECK \_ ONLINE \_ ALL**                 | Verifica todas as condições, exceto CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS. As verificações de revogação são executadas em todos os certificados na cadeia, exceto pelo certificado raiz. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **CAPICOM \_ CHECK \_ OFFLINE \_ ALL**                | Verifica todas as condições, exceto CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS. As verificações de revogação são executadas em todos os certificados na cadeia, exceto pelo certificado raiz. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




