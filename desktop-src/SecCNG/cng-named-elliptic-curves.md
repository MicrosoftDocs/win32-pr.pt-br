---
description: A partir do Windows 10, a CNG fornece suporte para as seguintes curvas elípticas nomeadas (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Curvas elípticas nomeadas CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826816"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="93899-103">CNG denominada curvas elípticas</span><span class="sxs-lookup"><span data-stu-id="93899-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="93899-104">A partir do Windows 10, a CNG fornece suporte para as seguintes curvas elípticas nomeadas (ANSI X 9.62, X 9.63, FIPS 186-2).</span><span class="sxs-lookup"><span data-stu-id="93899-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="93899-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**\_Curva ECC de BCRYPT \_ \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-106">Requirement</span></span> | <span data-ttu-id="93899-107">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="93899-108">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-108">Name</span></span>              | <span data-ttu-id="93899-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="93899-109">curve25519</span></span>                                                  |
| <span data-ttu-id="93899-110">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-110">Standard</span></span>          | [<span data-ttu-id="93899-111">Curva 25519</span><span class="sxs-lookup"><span data-stu-id="93899-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="93899-112">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-112">Key size (bits)</span></span>   | <span data-ttu-id="93899-113">255</span><span class="sxs-lookup"><span data-stu-id="93899-113">255</span></span>                                                         |
| <span data-ttu-id="93899-114">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="93899-115">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-115">Object identifier</span></span> | <span data-ttu-id="93899-116">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93899-116">None</span></span>                                                        |



 

<span data-ttu-id="93899-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_BRAINPOOLP160R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-118">Requirement</span></span> | <span data-ttu-id="93899-119">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-120">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-120">Name</span></span>              | <span data-ttu-id="93899-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="93899-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-122">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-122">Standard</span></span>          | [<span data-ttu-id="93899-123">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-124">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-124">Key size (bits)</span></span>   | <span data-ttu-id="93899-125">160</span><span class="sxs-lookup"><span data-stu-id="93899-125">160</span></span>                                                                                                               |
| <span data-ttu-id="93899-126">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-126">TLS capable</span></span>       | <span data-ttu-id="93899-127">Não</span><span class="sxs-lookup"><span data-stu-id="93899-127">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-128">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-128">Object identifier</span></span> | <span data-ttu-id="93899-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="93899-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="93899-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-131">Requirement</span></span> | <span data-ttu-id="93899-132">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-133">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-133">Name</span></span>              | <span data-ttu-id="93899-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="93899-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-135">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-135">Standard</span></span>          | [<span data-ttu-id="93899-136">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-137">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-137">Key size (bits)</span></span>   | <span data-ttu-id="93899-138">160</span><span class="sxs-lookup"><span data-stu-id="93899-138">160</span></span>                                                                                                               |
| <span data-ttu-id="93899-139">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-139">TLS capable</span></span>       | <span data-ttu-id="93899-140">Não</span><span class="sxs-lookup"><span data-stu-id="93899-140">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-141">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-141">Object identifier</span></span> | <span data-ttu-id="93899-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="93899-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="93899-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_BRAINPOOLP192R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-144">Requirement</span></span> | <span data-ttu-id="93899-145">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-146">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-146">Name</span></span>              | <span data-ttu-id="93899-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="93899-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-148">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-148">Standard</span></span>          | [<span data-ttu-id="93899-149">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-150">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-150">Key size (bits)</span></span>   | <span data-ttu-id="93899-151">192</span><span class="sxs-lookup"><span data-stu-id="93899-151">192</span></span>                                                                                                               |
| <span data-ttu-id="93899-152">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-152">TLS capable</span></span>       | <span data-ttu-id="93899-153">Não</span><span class="sxs-lookup"><span data-stu-id="93899-153">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-154">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-154">Object identifier</span></span> | <span data-ttu-id="93899-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="93899-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="93899-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_BRAINPOOLP192T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-157">Requirement</span></span> | <span data-ttu-id="93899-158">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-159">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-159">Name</span></span>              | <span data-ttu-id="93899-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="93899-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-161">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-161">Standard</span></span>          | [<span data-ttu-id="93899-162">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-163">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-163">Key size (bits)</span></span>   | <span data-ttu-id="93899-164">192</span><span class="sxs-lookup"><span data-stu-id="93899-164">192</span></span>                                                                                                               |
| <span data-ttu-id="93899-165">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-165">TLS capable</span></span>       | <span data-ttu-id="93899-166">Não</span><span class="sxs-lookup"><span data-stu-id="93899-166">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-167">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-167">Object identifier</span></span> | <span data-ttu-id="93899-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="93899-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="93899-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_BRAINPOOLP224R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-170">Requirement</span></span> | <span data-ttu-id="93899-171">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-172">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-172">Name</span></span>              | <span data-ttu-id="93899-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="93899-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-174">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-174">Standard</span></span>          | [<span data-ttu-id="93899-175">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-176">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-176">Key size (bits)</span></span>   | <span data-ttu-id="93899-177">224</span><span class="sxs-lookup"><span data-stu-id="93899-177">224</span></span>                                                                                                               |
| <span data-ttu-id="93899-178">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-178">TLS capable</span></span>       | <span data-ttu-id="93899-179">Não</span><span class="sxs-lookup"><span data-stu-id="93899-179">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-180">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-180">Object identifier</span></span> | <span data-ttu-id="93899-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="93899-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="93899-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_BRAINPOOLP224T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-183">Requirement</span></span> | <span data-ttu-id="93899-184">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-185">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-185">Name</span></span>              | <span data-ttu-id="93899-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="93899-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-187">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-187">Standard</span></span>          | [<span data-ttu-id="93899-188">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-189">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-189">Key size (bits)</span></span>   | <span data-ttu-id="93899-190">224</span><span class="sxs-lookup"><span data-stu-id="93899-190">224</span></span>                                                                                                               |
| <span data-ttu-id="93899-191">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-191">TLS capable</span></span>       | <span data-ttu-id="93899-192">Não</span><span class="sxs-lookup"><span data-stu-id="93899-192">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-193">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-193">Object identifier</span></span> | <span data-ttu-id="93899-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="93899-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="93899-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_BRAINPOOLP256R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-196">Requirement</span></span> | <span data-ttu-id="93899-197">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-198">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-198">Name</span></span>              | <span data-ttu-id="93899-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="93899-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-200">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-200">Standard</span></span>          | [<span data-ttu-id="93899-201">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-202">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-202">Key size (bits)</span></span>   | <span data-ttu-id="93899-203">256</span><span class="sxs-lookup"><span data-stu-id="93899-203">256</span></span>                                                                                                               |
| <span data-ttu-id="93899-204">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-204">TLS capable</span></span>       | <span data-ttu-id="93899-205">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="93899-206">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-206">Object identifier</span></span> | <span data-ttu-id="93899-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="93899-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="93899-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_BRAINPOOLP256T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-209">Requirement</span></span> | <span data-ttu-id="93899-210">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-211">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-211">Name</span></span>              | <span data-ttu-id="93899-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="93899-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-213">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-213">Standard</span></span>          | [<span data-ttu-id="93899-214">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-215">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-215">Key size (bits)</span></span>   | <span data-ttu-id="93899-216">256</span><span class="sxs-lookup"><span data-stu-id="93899-216">256</span></span>                                                                                                               |
| <span data-ttu-id="93899-217">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-217">TLS capable</span></span>       | <span data-ttu-id="93899-218">Não</span><span class="sxs-lookup"><span data-stu-id="93899-218">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-219">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-219">Object identifier</span></span> | <span data-ttu-id="93899-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="93899-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="93899-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_BRAINPOOLP320R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-222">Requirement</span></span> | <span data-ttu-id="93899-223">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-224">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-224">Name</span></span>              | <span data-ttu-id="93899-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="93899-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-226">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-226">Standard</span></span>          | [<span data-ttu-id="93899-227">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-228">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-228">Key size (bits)</span></span>   | <span data-ttu-id="93899-229">320</span><span class="sxs-lookup"><span data-stu-id="93899-229">320</span></span>                                                                                                               |
| <span data-ttu-id="93899-230">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-230">TLS capable</span></span>       | <span data-ttu-id="93899-231">Não</span><span class="sxs-lookup"><span data-stu-id="93899-231">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-232">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-232">Object identifier</span></span> | <span data-ttu-id="93899-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="93899-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="93899-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**\_ \_ BRAINPOOLP32 0T1 de curva de BCRYPT ECC \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-235">Requirement</span></span> | <span data-ttu-id="93899-236">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-237">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-237">Name</span></span>              | <span data-ttu-id="93899-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="93899-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-239">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-239">Standard</span></span>          | [<span data-ttu-id="93899-240">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-241">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-241">Key size (bits)</span></span>   | <span data-ttu-id="93899-242">320</span><span class="sxs-lookup"><span data-stu-id="93899-242">320</span></span>                                                                                                               |
| <span data-ttu-id="93899-243">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-243">TLS capable</span></span>       | <span data-ttu-id="93899-244">Não</span><span class="sxs-lookup"><span data-stu-id="93899-244">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-245">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-245">Object identifier</span></span> | <span data-ttu-id="93899-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="93899-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="93899-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-248">Requirement</span></span> | <span data-ttu-id="93899-249">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-250">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-250">Name</span></span>              | <span data-ttu-id="93899-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="93899-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-252">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-252">Standard</span></span>          | [<span data-ttu-id="93899-253">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-254">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-254">Key size (bits)</span></span>   | <span data-ttu-id="93899-255">384</span><span class="sxs-lookup"><span data-stu-id="93899-255">384</span></span>                                                                                                               |
| <span data-ttu-id="93899-256">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-256">TLS capable</span></span>       | <span data-ttu-id="93899-257">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="93899-258">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-258">Object identifier</span></span> | <span data-ttu-id="93899-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="93899-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="93899-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_BRAINPOOLP384T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-261">Requirement</span></span> | <span data-ttu-id="93899-262">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-263">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-263">Name</span></span>              | <span data-ttu-id="93899-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="93899-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-265">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-265">Standard</span></span>          | [<span data-ttu-id="93899-266">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-267">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-267">Key size (bits)</span></span>   | <span data-ttu-id="93899-268">384</span><span class="sxs-lookup"><span data-stu-id="93899-268">384</span></span>                                                                                                               |
| <span data-ttu-id="93899-269">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-269">TLS capable</span></span>       | <span data-ttu-id="93899-270">Não</span><span class="sxs-lookup"><span data-stu-id="93899-270">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-271">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-271">Object identifier</span></span> | <span data-ttu-id="93899-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="93899-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="93899-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_BRAINPOOLP512R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-274">Requirement</span></span> | <span data-ttu-id="93899-275">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-276">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-276">Name</span></span>              | <span data-ttu-id="93899-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="93899-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="93899-278">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-278">Standard</span></span>          | [<span data-ttu-id="93899-279">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-280">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-280">Key size (bits)</span></span>   | <span data-ttu-id="93899-281">512</span><span class="sxs-lookup"><span data-stu-id="93899-281">512</span></span>                                                                                                               |
| <span data-ttu-id="93899-282">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-282">TLS capable</span></span>       | <span data-ttu-id="93899-283">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="93899-284">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-284">Object identifier</span></span> | <span data-ttu-id="93899-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="93899-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="93899-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_BRAINPOOLP512T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-287">Requirement</span></span> | <span data-ttu-id="93899-288">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-289">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-289">Name</span></span>              | <span data-ttu-id="93899-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="93899-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="93899-291">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-291">Standard</span></span>          | [<span data-ttu-id="93899-292">Curvas padrão ECC brainpool e geração de curva</span><span class="sxs-lookup"><span data-stu-id="93899-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="93899-293">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-293">Key size (bits)</span></span>   | <span data-ttu-id="93899-294">512</span><span class="sxs-lookup"><span data-stu-id="93899-294">512</span></span>                                                                                                               |
| <span data-ttu-id="93899-295">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-295">TLS capable</span></span>       | <span data-ttu-id="93899-296">Não</span><span class="sxs-lookup"><span data-stu-id="93899-296">No</span></span>                                                                                                                |
| <span data-ttu-id="93899-297">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-297">Object identifier</span></span> | <span data-ttu-id="93899-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="93899-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="93899-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-300">Requirement</span></span> | <span data-ttu-id="93899-301">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="93899-302">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-302">Name</span></span>              | <span data-ttu-id="93899-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="93899-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="93899-304">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-304">Standard</span></span>          | <span data-ttu-id="93899-305">Chinês nacional padrão para LANs sem fio (GB 15629.11-2003)</span><span class="sxs-lookup"><span data-stu-id="93899-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="93899-306">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-306">Key size (bits)</span></span>   | <span data-ttu-id="93899-307">192</span><span class="sxs-lookup"><span data-stu-id="93899-307">192</span></span>                                                            |
| <span data-ttu-id="93899-308">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-308">TLS capable</span></span>       | <span data-ttu-id="93899-309">Não</span><span class="sxs-lookup"><span data-stu-id="93899-309">No</span></span>                                                             |
| <span data-ttu-id="93899-310">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-310">Object identifier</span></span> | <span data-ttu-id="93899-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="93899-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="93899-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_NISTP192 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-313">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-313">Requirement</span></span> | <span data-ttu-id="93899-314">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-315">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-315">Name</span></span>              | <span data-ttu-id="93899-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="93899-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="93899-317">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-317">Standard</span></span>          | [<span data-ttu-id="93899-318">Curvas elípticas recomendadas para uso do governo federal</span><span class="sxs-lookup"><span data-stu-id="93899-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="93899-319">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-319">Key size (bits)</span></span>   | <span data-ttu-id="93899-320">192</span><span class="sxs-lookup"><span data-stu-id="93899-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="93899-321">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-321">TLS capable</span></span>       | <span data-ttu-id="93899-322">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="93899-323">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-323">Object identifier</span></span> | <span data-ttu-id="93899-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="93899-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="93899-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-326">Requirement</span></span> | <span data-ttu-id="93899-327">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-328">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-328">Name</span></span>              | <span data-ttu-id="93899-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="93899-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="93899-330">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-330">Standard</span></span>          | [<span data-ttu-id="93899-331">Curvas elípticas recomendadas para uso do governo federal</span><span class="sxs-lookup"><span data-stu-id="93899-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="93899-332">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-332">Key size (bits)</span></span>   | <span data-ttu-id="93899-333">224</span><span class="sxs-lookup"><span data-stu-id="93899-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="93899-334">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-334">TLS capable</span></span>       | <span data-ttu-id="93899-335">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="93899-336">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-336">Object identifier</span></span> | <span data-ttu-id="93899-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="93899-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="93899-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_NISTP256 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-339">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-339">Requirement</span></span> | <span data-ttu-id="93899-340">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-341">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-341">Name</span></span>              | <span data-ttu-id="93899-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="93899-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="93899-343">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-343">Standard</span></span>          | [<span data-ttu-id="93899-344">Curvas elípticas recomendadas para uso do governo federal</span><span class="sxs-lookup"><span data-stu-id="93899-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="93899-345">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-345">Key size (bits)</span></span>   | <span data-ttu-id="93899-346">256</span><span class="sxs-lookup"><span data-stu-id="93899-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="93899-347">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-347">TLS capable</span></span>       | <span data-ttu-id="93899-348">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="93899-349">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-349">Object identifier</span></span> | <span data-ttu-id="93899-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="93899-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="93899-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-352">Requirement</span></span> | <span data-ttu-id="93899-353">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-354">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-354">Name</span></span>              | <span data-ttu-id="93899-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="93899-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="93899-356">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-356">Standard</span></span>          | [<span data-ttu-id="93899-357">Curvas elípticas recomendadas para uso do governo federal</span><span class="sxs-lookup"><span data-stu-id="93899-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="93899-358">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-358">Key size (bits)</span></span>   | <span data-ttu-id="93899-359">384</span><span class="sxs-lookup"><span data-stu-id="93899-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="93899-360">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-360">TLS capable</span></span>       | <span data-ttu-id="93899-361">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="93899-362">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-362">Object identifier</span></span> | <span data-ttu-id="93899-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="93899-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="93899-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_NISTP521 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-365">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-365">Requirement</span></span> | <span data-ttu-id="93899-366">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-367">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-367">Name</span></span>              | <span data-ttu-id="93899-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="93899-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="93899-369">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-369">Standard</span></span>          | [<span data-ttu-id="93899-370">Curvas elípticas recomendadas para uso do governo federal</span><span class="sxs-lookup"><span data-stu-id="93899-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="93899-371">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-371">Key size (bits)</span></span>   | <span data-ttu-id="93899-372">521</span><span class="sxs-lookup"><span data-stu-id="93899-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="93899-373">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-373">TLS capable</span></span>       | <span data-ttu-id="93899-374">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="93899-375">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-375">Object identifier</span></span> | <span data-ttu-id="93899-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="93899-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="93899-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-378">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-378">Requirement</span></span> | <span data-ttu-id="93899-379">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-380">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-380">Name</span></span>              | <span data-ttu-id="93899-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="93899-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="93899-382">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-382">Standard</span></span>          | [<span data-ttu-id="93899-383">Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR</span><span class="sxs-lookup"><span data-stu-id="93899-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="93899-384">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-384">Key size (bits)</span></span>   | <span data-ttu-id="93899-385">256</span><span class="sxs-lookup"><span data-stu-id="93899-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="93899-386">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-386">TLS capable</span></span>       | <span data-ttu-id="93899-387">Não</span><span class="sxs-lookup"><span data-stu-id="93899-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="93899-388">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-388">Object identifier</span></span> | <span data-ttu-id="93899-389">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93899-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="93899-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-391">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-391">Requirement</span></span> | <span data-ttu-id="93899-392">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-393">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-393">Name</span></span>              | <span data-ttu-id="93899-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="93899-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="93899-395">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-395">Standard</span></span>          | [<span data-ttu-id="93899-396">Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR</span><span class="sxs-lookup"><span data-stu-id="93899-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="93899-397">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-397">Key size (bits)</span></span>   | <span data-ttu-id="93899-398">384</span><span class="sxs-lookup"><span data-stu-id="93899-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="93899-399">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-399">TLS capable</span></span>       | <span data-ttu-id="93899-400">Não</span><span class="sxs-lookup"><span data-stu-id="93899-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="93899-401">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-401">Object identifier</span></span> | <span data-ttu-id="93899-402">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93899-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="93899-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_NUMSP512T1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-404">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-404">Requirement</span></span> | <span data-ttu-id="93899-405">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-406">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-406">Name</span></span>              | <span data-ttu-id="93899-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="93899-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="93899-408">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-408">Standard</span></span>          | [<span data-ttu-id="93899-409">Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR</span><span class="sxs-lookup"><span data-stu-id="93899-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="93899-410">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-410">Key size (bits)</span></span>   | <span data-ttu-id="93899-411">512</span><span class="sxs-lookup"><span data-stu-id="93899-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="93899-412">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-412">TLS capable</span></span>       | <span data-ttu-id="93899-413">Não</span><span class="sxs-lookup"><span data-stu-id="93899-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="93899-414">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-414">Object identifier</span></span> | <span data-ttu-id="93899-415">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93899-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="93899-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-417">Requirement</span></span> | <span data-ttu-id="93899-418">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-419">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-419">Name</span></span>              | <span data-ttu-id="93899-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="93899-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="93899-421">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-421">Standard</span></span>          | [<span data-ttu-id="93899-422">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-423">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-423">Key size (bits)</span></span>   | <span data-ttu-id="93899-424">160</span><span class="sxs-lookup"><span data-stu-id="93899-424">160</span></span>                                                                             |
| <span data-ttu-id="93899-425">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-425">TLS capable</span></span>       | <span data-ttu-id="93899-426">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-426">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-427">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-427">Object identifier</span></span> | <span data-ttu-id="93899-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="93899-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="93899-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-430">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-430">Requirement</span></span> | <span data-ttu-id="93899-431">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-432">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-432">Name</span></span>              | <span data-ttu-id="93899-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="93899-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="93899-434">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-434">Standard</span></span>          | [<span data-ttu-id="93899-435">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-436">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-436">Key size (bits)</span></span>   | <span data-ttu-id="93899-437">160</span><span class="sxs-lookup"><span data-stu-id="93899-437">160</span></span>                                                                             |
| <span data-ttu-id="93899-438">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-438">TLS capable</span></span>       | <span data-ttu-id="93899-439">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-439">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-440">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-440">Object identifier</span></span> | <span data-ttu-id="93899-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="93899-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="93899-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-443">Requirement</span></span> | <span data-ttu-id="93899-444">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-445">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-445">Name</span></span>              | <span data-ttu-id="93899-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="93899-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="93899-447">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-447">Standard</span></span>          | [<span data-ttu-id="93899-448">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-449">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-449">Key size (bits)</span></span>   | <span data-ttu-id="93899-450">160</span><span class="sxs-lookup"><span data-stu-id="93899-450">160</span></span>                                                                             |
| <span data-ttu-id="93899-451">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-451">TLS capable</span></span>       | <span data-ttu-id="93899-452">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-452">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-453">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-453">Object identifier</span></span> | <span data-ttu-id="93899-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="93899-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="93899-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_SECP192K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-456">Requirement</span></span> | <span data-ttu-id="93899-457">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-458">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-458">Name</span></span>              | <span data-ttu-id="93899-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="93899-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="93899-460">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-460">Standard</span></span>          | [<span data-ttu-id="93899-461">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-462">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-462">Key size (bits)</span></span>   | <span data-ttu-id="93899-463">192</span><span class="sxs-lookup"><span data-stu-id="93899-463">192</span></span>                                                                             |
| <span data-ttu-id="93899-464">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-464">TLS capable</span></span>       | <span data-ttu-id="93899-465">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-465">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-466">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-466">Object identifier</span></span> | <span data-ttu-id="93899-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="93899-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="93899-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-469">Requirement</span></span> | <span data-ttu-id="93899-470">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-471">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-471">Name</span></span>              | <span data-ttu-id="93899-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="93899-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="93899-473">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-473">Standard</span></span>          | [<span data-ttu-id="93899-474">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-475">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-475">Key size (bits)</span></span>   | <span data-ttu-id="93899-476">192</span><span class="sxs-lookup"><span data-stu-id="93899-476">192</span></span>                                                                             |
| <span data-ttu-id="93899-477">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-477">TLS capable</span></span>       | <span data-ttu-id="93899-478">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-478">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-479">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-479">Object identifier</span></span> | <span data-ttu-id="93899-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="93899-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="93899-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_SECP224K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-482">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-482">Requirement</span></span> | <span data-ttu-id="93899-483">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-484">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-484">Name</span></span>              | <span data-ttu-id="93899-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="93899-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="93899-486">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-486">Standard</span></span>          | [<span data-ttu-id="93899-487">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-488">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-488">Key size (bits)</span></span>   | <span data-ttu-id="93899-489">224</span><span class="sxs-lookup"><span data-stu-id="93899-489">224</span></span>                                                                             |
| <span data-ttu-id="93899-490">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-490">TLS capable</span></span>       | <span data-ttu-id="93899-491">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-491">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-492">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-492">Object identifier</span></span> | <span data-ttu-id="93899-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="93899-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="93899-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_SECP224R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-495">Requirement</span></span> | <span data-ttu-id="93899-496">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-497">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-497">Name</span></span>              | <span data-ttu-id="93899-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="93899-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="93899-499">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-499">Standard</span></span>          | [<span data-ttu-id="93899-500">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-501">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-501">Key size (bits)</span></span>   | <span data-ttu-id="93899-502">224</span><span class="sxs-lookup"><span data-stu-id="93899-502">224</span></span>                                                                             |
| <span data-ttu-id="93899-503">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-503">TLS capable</span></span>       | <span data-ttu-id="93899-504">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-504">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-505">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-505">Object identifier</span></span> | <span data-ttu-id="93899-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="93899-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="93899-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_SECP256K1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-508">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-508">Requirement</span></span> | <span data-ttu-id="93899-509">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-510">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-510">Name</span></span>              | <span data-ttu-id="93899-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="93899-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="93899-512">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-512">Standard</span></span>          | [<span data-ttu-id="93899-513">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-514">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-514">Key size (bits)</span></span>   | <span data-ttu-id="93899-515">256</span><span class="sxs-lookup"><span data-stu-id="93899-515">256</span></span>                                                                             |
| <span data-ttu-id="93899-516">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-516">TLS capable</span></span>       | <span data-ttu-id="93899-517">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-517">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-518">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-518">Object identifier</span></span> | <span data-ttu-id="93899-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="93899-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="93899-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_SECP256R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-521">Requirement</span></span> | <span data-ttu-id="93899-522">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-523">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-523">Name</span></span>              | <span data-ttu-id="93899-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="93899-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="93899-525">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-525">Standard</span></span>          | [<span data-ttu-id="93899-526">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-527">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-527">Key size (bits)</span></span>   | <span data-ttu-id="93899-528">256</span><span class="sxs-lookup"><span data-stu-id="93899-528">256</span></span>                                                                             |
| <span data-ttu-id="93899-529">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-529">TLS capable</span></span>       | <span data-ttu-id="93899-530">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-530">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-531">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-531">Object identifier</span></span> | <span data-ttu-id="93899-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="93899-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="93899-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-534">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-534">Requirement</span></span> | <span data-ttu-id="93899-535">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-536">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-536">Name</span></span>              | <span data-ttu-id="93899-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="93899-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="93899-538">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-538">Standard</span></span>          | [<span data-ttu-id="93899-539">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-540">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-540">Key size (bits)</span></span>   | <span data-ttu-id="93899-541">384</span><span class="sxs-lookup"><span data-stu-id="93899-541">384</span></span>                                                                             |
| <span data-ttu-id="93899-542">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-542">TLS capable</span></span>       | <span data-ttu-id="93899-543">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-543">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-544">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-544">Object identifier</span></span> | <span data-ttu-id="93899-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="93899-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="93899-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_SECP521R1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-547">Requirement</span></span> | <span data-ttu-id="93899-548">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="93899-549">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-549">Name</span></span>              | <span data-ttu-id="93899-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="93899-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="93899-551">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-551">Standard</span></span>          | [<span data-ttu-id="93899-552">Parâmetros de domínio de curva elíptica recomendados</span><span class="sxs-lookup"><span data-stu-id="93899-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="93899-553">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-553">Key size (bits)</span></span>   | <span data-ttu-id="93899-554">521</span><span class="sxs-lookup"><span data-stu-id="93899-554">521</span></span>                                                                             |
| <span data-ttu-id="93899-555">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-555">TLS capable</span></span>       | <span data-ttu-id="93899-556">Sim</span><span class="sxs-lookup"><span data-stu-id="93899-556">Yes</span></span>                                                                             |
| <span data-ttu-id="93899-557">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-557">Object identifier</span></span> | <span data-ttu-id="93899-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="93899-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="93899-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_WTLS12 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-560">Requirement</span></span> | <span data-ttu-id="93899-561">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="93899-562">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-562">Name</span></span>              | <span data-ttu-id="93899-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="93899-563">wtls12</span></span>       |
| <span data-ttu-id="93899-564">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-564">Standard</span></span>          | <span data-ttu-id="93899-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="93899-565">WTLS</span></span>         |
| <span data-ttu-id="93899-566">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-566">Key size (bits)</span></span>   | <span data-ttu-id="93899-567">224</span><span class="sxs-lookup"><span data-stu-id="93899-567">224</span></span>          |
| <span data-ttu-id="93899-568">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-568">TLS capable</span></span>       | <span data-ttu-id="93899-569">Não</span><span class="sxs-lookup"><span data-stu-id="93899-569">No</span></span>           |
| <span data-ttu-id="93899-570">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-570">Object identifier</span></span> | <span data-ttu-id="93899-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="93899-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="93899-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_WTLS7 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-573">Requirement</span></span> | <span data-ttu-id="93899-574">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="93899-575">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-575">Name</span></span>              | <span data-ttu-id="93899-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="93899-576">wtls7</span></span>        |
| <span data-ttu-id="93899-577">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-577">Standard</span></span>          | <span data-ttu-id="93899-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="93899-578">WTLS</span></span>         |
| <span data-ttu-id="93899-579">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-579">Key size (bits)</span></span>   | <span data-ttu-id="93899-580">160</span><span class="sxs-lookup"><span data-stu-id="93899-580">160</span></span>          |
| <span data-ttu-id="93899-581">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-581">TLS capable</span></span>       | <span data-ttu-id="93899-582">Não</span><span class="sxs-lookup"><span data-stu-id="93899-582">No</span></span>           |
| <span data-ttu-id="93899-583">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-583">Object identifier</span></span> | <span data-ttu-id="93899-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="93899-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="93899-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-586">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-586">Requirement</span></span> | <span data-ttu-id="93899-587">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="93899-588">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-588">Name</span></span>              | <span data-ttu-id="93899-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="93899-589">wtls9</span></span>         |
| <span data-ttu-id="93899-590">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-590">Standard</span></span>          | <span data-ttu-id="93899-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="93899-591">WTLS</span></span>          |
| <span data-ttu-id="93899-592">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-592">Key size (bits)</span></span>   | <span data-ttu-id="93899-593">160</span><span class="sxs-lookup"><span data-stu-id="93899-593">160</span></span>           |
| <span data-ttu-id="93899-594">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-594">TLS capable</span></span>       | <span data-ttu-id="93899-595">Não</span><span class="sxs-lookup"><span data-stu-id="93899-595">No</span></span>            |
| <span data-ttu-id="93899-596">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-596">Object identifier</span></span> | <span data-ttu-id="93899-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="93899-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="93899-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_X962P192V1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-599">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-599">Requirement</span></span> | <span data-ttu-id="93899-600">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-601">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-601">Name</span></span>              | <span data-ttu-id="93899-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="93899-602">x962P192v1</span></span>          |
| <span data-ttu-id="93899-603">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-603">Standard</span></span>          | <span data-ttu-id="93899-604">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-605">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-605">Key size (bits)</span></span>   | <span data-ttu-id="93899-606">192</span><span class="sxs-lookup"><span data-stu-id="93899-606">192</span></span>                 |
| <span data-ttu-id="93899-607">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-607">TLS capable</span></span>       | <span data-ttu-id="93899-608">Não</span><span class="sxs-lookup"><span data-stu-id="93899-608">No</span></span>                  |
| <span data-ttu-id="93899-609">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-609">Object identifier</span></span> | <span data-ttu-id="93899-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="93899-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="93899-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-612">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-612">Requirement</span></span> | <span data-ttu-id="93899-613">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-614">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-614">Name</span></span>              | <span data-ttu-id="93899-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="93899-615">x962P192v2</span></span>          |
| <span data-ttu-id="93899-616">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-616">Standard</span></span>          | <span data-ttu-id="93899-617">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-618">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-618">Key size (bits)</span></span>   | <span data-ttu-id="93899-619">192</span><span class="sxs-lookup"><span data-stu-id="93899-619">192</span></span>                 |
| <span data-ttu-id="93899-620">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-620">TLS capable</span></span>       | <span data-ttu-id="93899-621">Não</span><span class="sxs-lookup"><span data-stu-id="93899-621">No</span></span>                  |
| <span data-ttu-id="93899-622">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-622">Object identifier</span></span> | <span data-ttu-id="93899-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="93899-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="93899-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_X962P192V3 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-625">Requirement</span></span> | <span data-ttu-id="93899-626">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-627">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-627">Name</span></span>              | <span data-ttu-id="93899-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="93899-628">x962P192v3</span></span>          |
| <span data-ttu-id="93899-629">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-629">Standard</span></span>          | <span data-ttu-id="93899-630">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-631">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-631">Key size (bits)</span></span>   | <span data-ttu-id="93899-632">192</span><span class="sxs-lookup"><span data-stu-id="93899-632">192</span></span>                 |
| <span data-ttu-id="93899-633">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-633">TLS capable</span></span>       | <span data-ttu-id="93899-634">Não</span><span class="sxs-lookup"><span data-stu-id="93899-634">No</span></span>                  |
| <span data-ttu-id="93899-635">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-635">Object identifier</span></span> | <span data-ttu-id="93899-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="93899-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="93899-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-638">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-638">Requirement</span></span> | <span data-ttu-id="93899-639">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-640">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-640">Name</span></span>              | <span data-ttu-id="93899-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="93899-641">x962P239v1</span></span>          |
| <span data-ttu-id="93899-642">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-642">Standard</span></span>          | <span data-ttu-id="93899-643">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-644">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-644">Key size (bits)</span></span>   | <span data-ttu-id="93899-645">239</span><span class="sxs-lookup"><span data-stu-id="93899-645">239</span></span>                 |
| <span data-ttu-id="93899-646">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-646">TLS capable</span></span>       | <span data-ttu-id="93899-647">Não</span><span class="sxs-lookup"><span data-stu-id="93899-647">No</span></span>                  |
| <span data-ttu-id="93899-648">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-648">Object identifier</span></span> | <span data-ttu-id="93899-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="93899-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="93899-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-651">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-651">Requirement</span></span> | <span data-ttu-id="93899-652">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-653">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-653">Name</span></span>              | <span data-ttu-id="93899-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="93899-654">x962P239v2</span></span>          |
| <span data-ttu-id="93899-655">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-655">Standard</span></span>          | <span data-ttu-id="93899-656">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-657">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-657">Key size (bits)</span></span>   | <span data-ttu-id="93899-658">239</span><span class="sxs-lookup"><span data-stu-id="93899-658">239</span></span>                 |
| <span data-ttu-id="93899-659">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-659">TLS capable</span></span>       | <span data-ttu-id="93899-660">Não</span><span class="sxs-lookup"><span data-stu-id="93899-660">No</span></span>                  |
| <span data-ttu-id="93899-661">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-661">Object identifier</span></span> | <span data-ttu-id="93899-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="93899-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="93899-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 de curva ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-664">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-664">Requirement</span></span> | <span data-ttu-id="93899-665">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-666">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-666">Name</span></span>              | <span data-ttu-id="93899-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="93899-667">x962P239v3</span></span>          |
| <span data-ttu-id="93899-668">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-668">Standard</span></span>          | <span data-ttu-id="93899-669">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-670">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-670">Key size (bits)</span></span>   | <span data-ttu-id="93899-671">239</span><span class="sxs-lookup"><span data-stu-id="93899-671">239</span></span>                 |
| <span data-ttu-id="93899-672">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-672">TLS capable</span></span>       | <span data-ttu-id="93899-673">Não</span><span class="sxs-lookup"><span data-stu-id="93899-673">No</span></span>                  |
| <span data-ttu-id="93899-674">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-674">Object identifier</span></span> | <span data-ttu-id="93899-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="93899-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="93899-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_X962P256V1 de \_ curva de ECC BCRYPT \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="93899-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="93899-677">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-677">Requirement</span></span> | <span data-ttu-id="93899-678">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="93899-679">Nome</span><span class="sxs-lookup"><span data-stu-id="93899-679">Name</span></span>              | <span data-ttu-id="93899-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="93899-680">x962P256v1</span></span>          |
| <span data-ttu-id="93899-681">Standard</span><span class="sxs-lookup"><span data-stu-id="93899-681">Standard</span></span>          | <span data-ttu-id="93899-682">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="93899-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="93899-683">Tamanho da chave (bits)</span><span class="sxs-lookup"><span data-stu-id="93899-683">Key size (bits)</span></span>   | <span data-ttu-id="93899-684">256</span><span class="sxs-lookup"><span data-stu-id="93899-684">256</span></span>                 |
| <span data-ttu-id="93899-685">Compatível com TLS</span><span class="sxs-lookup"><span data-stu-id="93899-685">TLS capable</span></span>       | <span data-ttu-id="93899-686">Não</span><span class="sxs-lookup"><span data-stu-id="93899-686">No</span></span>                  |
| <span data-ttu-id="93899-687">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="93899-687">Object identifier</span></span> | <span data-ttu-id="93899-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="93899-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93899-689">Comentários</span><span class="sxs-lookup"><span data-stu-id="93899-689">Remarks</span></span>

<span data-ttu-id="93899-690">Para usar uma curva nomeada, chame [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) usando o **algoritmo de \_ ECDSA \_ BCrypt** ou o **\_ \_ algoritmo BCrypt ECDH** como a ID do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="93899-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="93899-691">Em seguida, chame [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) e defina a propriedade de nome de **\_ \_ curva \_ de ECC BCRYPT** como uma das curvas acima ou quaisquer curvas nomeadas registradas no computador, conforme mostrado pelo `certutil -displayEccCurve` comando.</span><span class="sxs-lookup"><span data-stu-id="93899-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="93899-692">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93899-692">Requirements</span></span>



| <span data-ttu-id="93899-693">Requisito</span><span class="sxs-lookup"><span data-stu-id="93899-693">Requirement</span></span> | <span data-ttu-id="93899-694">Valor</span><span class="sxs-lookup"><span data-stu-id="93899-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93899-695">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93899-695">Minimum supported client</span></span><br/> | <span data-ttu-id="93899-696">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="93899-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="93899-697">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93899-697">Minimum supported server</span></span><br/> | <span data-ttu-id="93899-698">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="93899-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="93899-699">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93899-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="93899-700"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="93899-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93899-701">Confira também</span><span class="sxs-lookup"><span data-stu-id="93899-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93899-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="93899-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="93899-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="93899-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




