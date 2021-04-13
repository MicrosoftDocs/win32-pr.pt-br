---
description: O método GetValuesForProp retorna todos os valores de uma determinada propriedade que são gerados por essa propriedade como aparece dentro da consulta.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'Métodos CFrameworkQuery:: GetValuesForProp (FrQuery. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170623"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>Métodos CFrameworkQuery:: GetValuesForProp

\[A classe [**CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O método **GetValuesForProp** retorna todos os valores de uma determinada propriedade que são gerados por essa propriedade como aparece dentro da consulta.

Por exemplo, uma chamada para **GetValuesForProp**(L "Name", SA) retorna a matriz *SA*, que contém todos os valores de "Name" que exigem que as instâncias sejam enviadas de volta para atender à consulta. Se *SA* contiver {"a", "b"}, todas as instâncias em que "Name = a" e todas as instâncias em que "Name = b" deverão ser enviadas de volta para atender completamente à consulta.

Se as restrições em "Name" não forem uma limitação suficientemente, uma matriz *SA* vazia será retornada.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                             | Descrição                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp (CHStringArray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Retorna todos os valores de uma determinada propriedade que são gerados por essa propriedade como aparece dentro da consulta.<br/> |
| [**GetValuesForProp (LPCWSTR, std:: vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Retorna todos os valores de uma determinada propriedade que são gerados por essa propriedade como aparece dentro da consulta.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>FrQuery. h (incluir FwCommon. h)</dt> </dl>                                                     |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
